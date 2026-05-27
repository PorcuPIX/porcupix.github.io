---
title: Strudel：代码制作音乐
date: 2026-05-27 20:42:42
tags:
  - Strudel
  - 音乐编程
  - 游戏开发
categories:
  - 工具
description: 一个关于 Strudel 和游戏音乐原型的小记录。
---

介绍一个音乐工具 [Strudel](https://strudel.cc/workshop/getting-started/)，感觉挺适合随手做音乐草稿。

它可以直接在浏览器里用代码生成音乐。写几行 pattern，点一下播放，就能马上听到结果。这个体验和传统音乐软件不太一样，更像是在写一个会发声的小程序：旋律、鼓点、速度、音色都可以被代码控制。

在开发独立游戏时可以 vibe coding 出一段小 loop

下面是一个简单的小旋律示例。

<script src="https://unpkg.com/@strudel/embed@latest"></script>

<strudel-repl>
<!--
setcps(0.72)
stack(
  // kick + snare
  sound("bd ~ ~ bd sd ~ ~ sd")
    .bank("RolandTR909")
    .gain(0.75),
  // hats
  sound("hh*8")
    .gain(0.18)
    .slow(2),
  // bass
  note("e2 ~ b1 ~ c2 ~ g1 ~")
    .sound("sawtooth")
    .lpf(500)
    .gain(0.22)
    .slow(2),
  // emotional synth lead
  note("e4 g4 b4 ~ d5 b4 g4 ~ c5 b4 g4 ~")
    .sound("triangle")
    .room(0.75)
    .delay(0.35)
    .gain(0.30)
    .slow(2),
  // ambient pad
  note("[e5,g5,b5] [d5,fs5,a5]")
    .sound("sine")
    .room(1)
    .gain(0.08)
    .slow(8)
)
._scope()
-->
</strudel-repl>
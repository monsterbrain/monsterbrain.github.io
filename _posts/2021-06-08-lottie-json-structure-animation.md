---
layout: post
title: Lottie JSON Structure for Animation
categories: Programming
---

Lottie ([Link](https://airbnb.io/lottie/)) is an awesome animation library for web, android and ios, for creating animation files from aftereffects. However if you want to edit a lottie json file, it's hard because the keys were abbreviated so as to reduce the size I guess.

There's no official record of this. So python [lottie](http://mattbas.gitlab.io/python-lottie/) docs had done a good job of decoding the json keys. Here are the main keys, I've extracted from their site.

## Animation
<table class="markdownTable">
<tr class="markdownTableHead">
<th class="markdownTableHeadNone">Lottie name </th><th class="markdownTableHeadNone">Type </th><th class="markdownTableHeadNone">Description </th><th class="markdownTableHeadNone">Attribute  </th></tr>
<tr class="markdownTableRowOdd">
<td class="markdownTableBodyNone">layers </td><td class="markdownTableBodyNone">list of <a href="#lottie_Layer">Layer</a> </td><td class="markdownTableBodyNone">List of Composition Layers. &#160; </td><td class="markdownTableBodyNone"><a class="el" href="classlottie_1_1objects_1_1composition_1_1Composition.html#a67f1330cb86190299da5fb4d660789fa">layers</a>  </td></tr>
<tr class="markdownTableRowEven">
<td class="markdownTableBodyNone">v </td><td class="markdownTableBodyNone">str </td><td class="markdownTableBodyNone">Bodymovin Version. &#160; </td><td class="markdownTableBodyNone"><a class="el" href="classlottie_1_1objects_1_1animation_1_1Animation.html#a1fce07d8e28b066de05b6ec377f27473">version</a>  </td></tr>
<tr class="markdownTableRowOdd">
<td class="markdownTableBodyNone">fr </td><td class="markdownTableBodyNone">float </td><td class="markdownTableBodyNone">Frames per second. &#160; </td><td class="markdownTableBodyNone"><a class="el" href="classlottie_1_1objects_1_1animation_1_1Animation.html#a658b7c25e7115a777d87136fc4346ce7">frame_rate</a>  </td></tr>
<tr class="markdownTableRowEven">
<td class="markdownTableBodyNone">ip </td><td class="markdownTableBodyNone">float </td><td class="markdownTableBodyNone">The time when the composition work area begins, in frames. &#160; </td><td class="markdownTableBodyNone"><a class="el" href="classlottie_1_1objects_1_1animation_1_1Animation.html#a22c370ffb91a20199f7e914d3618a6a9">in_point</a>  </td></tr>
<tr class="markdownTableRowOdd">
<td class="markdownTableBodyNone">op </td><td class="markdownTableBodyNone">float </td><td class="markdownTableBodyNone">The time when the composition work area ends. &#160; </td><td class="markdownTableBodyNone"><a class="el" href="classlottie_1_1objects_1_1animation_1_1Animation.html#aa5646c03a2f3a6034b2baeb1964e589d">out_point</a>  </td></tr>
<tr class="markdownTableRowEven">
<td class="markdownTableBodyNone">w </td><td class="markdownTableBodyNone">int </td><td class="markdownTableBodyNone">Composition Width. &#160; </td><td class="markdownTableBodyNone"><a class="el" href="classlottie_1_1objects_1_1animation_1_1Animation.html#a62e24d4885d26d5d2f4b093376902780">width</a>  </td></tr>
<tr class="markdownTableRowOdd">
<td class="markdownTableBodyNone">h </td><td class="markdownTableBodyNone">int </td><td class="markdownTableBodyNone">Composition Height. &#160; </td><td class="markdownTableBodyNone"><a class="el" href="classlottie_1_1objects_1_1animation_1_1Animation.html#a099701f682943ee8e2daa048cab218b9">height</a>  </td></tr>
<tr class="markdownTableRowEven">
<td class="markdownTableBodyNone">nm </td><td class="markdownTableBodyNone">str </td><td class="markdownTableBodyNone">Composition name. &#160; </td><td class="markdownTableBodyNone"><a class="el" href="classlottie_1_1objects_1_1animation_1_1Animation.html#a27a0953eab5fb862bf132a3f32dbff9c">name</a>  </td></tr>
<tr class="markdownTableRowOdd">
<td class="markdownTableBodyNone">ddd </td><td class="markdownTableBodyNone">0-1 int </td><td class="markdownTableBodyNone">Composition has 3-D layers. &#160; </td><td class="markdownTableBodyNone"><a class="el" href="classlottie_1_1objects_1_1animation_1_1Animation.html#a6a5e1220a9e874f38787523d982c28a2">threedimensional</a>  </td></tr>
<tr class="markdownTableRowEven">
<td class="markdownTableBodyNone">assets </td><td class="markdownTableBodyNone">list of <a href="#lottie_Asset">Asset</a> </td><td class="markdownTableBodyNone">source items that can be used in multiple places. &#160; </td><td class="markdownTableBodyNone"><a class="el" href="classlottie_1_1objects_1_1animation_1_1Animation.html#a96fd721eff2f9426157a9f22f0085ab9">assets</a>  </td></tr>
<tr class="markdownTableRowOdd">
<td class="markdownTableBodyNone">fonts </td><td class="markdownTableBodyNone"><a href="#lottie_FontList">FontList</a> </td><td class="markdownTableBodyNone">Available fonts. &#160; </td><td class="markdownTableBodyNone"><a class="el" href="classlottie_1_1objects_1_1animation_1_1Animation.html#ae0d3a29369e405a427ccad03c68c564e">fonts</a>  </td></tr>
<tr class="markdownTableRowEven">
<td class="markdownTableBodyNone">chars </td><td class="markdownTableBodyNone">list of <a href="#lottie_Chars">Chars</a> </td><td class="markdownTableBodyNone">source chars for text layers &#160; </td><td class="markdownTableBodyNone"><a class="el" href="classlottie_1_1objects_1_1animation_1_1Animation.html#a83853d562cdefbdcbf676eed309fe687">chars</a>  </td></tr>
</table>

## Image
<table class="markdownTable">
<tr class="markdownTableHead">
<th class="markdownTableHeadNone">Lottie name </th><th class="markdownTableHeadNone">Type </th><th class="markdownTableHeadNone">Description </th><th class="markdownTableHeadNone">Attribute  </th></tr>
<tr class="markdownTableRowOdd">
<td class="markdownTableBodyNone">h </td><td class="markdownTableBodyNone">float </td><td class="markdownTableBodyNone">Image Height. &#160; </td><td class="markdownTableBodyNone"><a class="el" href="classlottie_1_1objects_1_1assets_1_1Image.html#ab15b7b804f113a606514c555b8d93949">height</a>  </td></tr>
<tr class="markdownTableRowEven">
<td class="markdownTableBodyNone">w </td><td class="markdownTableBodyNone">float </td><td class="markdownTableBodyNone">Image Width. &#160; </td><td class="markdownTableBodyNone"><a class="el" href="classlottie_1_1objects_1_1assets_1_1Image.html#a3543cabf7bd39141d3c76c2cf71f594f">width</a>  </td></tr>
<tr class="markdownTableRowOdd">
<td class="markdownTableBodyNone">id </td><td class="markdownTableBodyNone">str </td><td class="markdownTableBodyNone">Image ID. &#160; </td><td class="markdownTableBodyNone"><a class="el" href="classlottie_1_1objects_1_1assets_1_1Image.html#a07a7cc7e028ee010723d1f53e28d70ed">id</a>  </td></tr>
<tr class="markdownTableRowEven">
<td class="markdownTableBodyNone">p </td><td class="markdownTableBodyNone">str </td><td class="markdownTableBodyNone">Image name. &#160; </td><td class="markdownTableBodyNone"><a class="el" href="classlottie_1_1objects_1_1assets_1_1Image.html#a042d787272cf713f95d00781a151b6bb">image</a>  </td></tr>
<tr class="markdownTableRowOdd">
<td class="markdownTableBodyNone">u </td><td class="markdownTableBodyNone">str </td><td class="markdownTableBodyNone">Image path. &#160; </td><td class="markdownTableBodyNone"><a class="el" href="classlottie_1_1objects_1_1assets_1_1Image.html#ab43fb8a3510c1d829447af8c84bf4189">image_path</a>  </td></tr>
<tr class="markdownTableRowEven">
<td class="markdownTableBodyNone">e </td><td class="markdownTableBodyNone">0-1 int </td><td class="markdownTableBodyNone">Image data is stored as a data: url. &#160; </td><td class="markdownTableBodyNone"><a class="el" href="classlottie_1_1objects_1_1assets_1_1Image.html#a35d44031d86bfc397632dc00a67f324a">is_embedded</a>  </td></tr>
</table>

## Transform
<table class="markdownTable">
<tr class="markdownTableHead">
<th class="markdownTableHeadNone">Lottie name </th><th class="markdownTableHeadNone">Type </th><th class="markdownTableHeadNone">Description </th><th class="markdownTableHeadNone">Attribute  </th></tr>
<tr class="markdownTableRowOdd">
<td class="markdownTableBodyNone">a </td><td class="markdownTableBodyNone"><a href="#lottie_MultiDimensional">MultiDimensional</a> </td><td class="markdownTableBodyNone">Transform Anchor Point. &#160; </td><td class="markdownTableBodyNone"><a class="el" href="classlottie_1_1objects_1_1helpers_1_1Transform.html#a0f3a683de74503ac72036b10882e7594">anchor_point</a>  </td></tr>
<tr class="markdownTableRowEven">
<td class="markdownTableBodyNone">p </td><td class="markdownTableBodyNone"><a href="#lottie_PositionValue">PositionValue</a> </td><td class="markdownTableBodyNone">Transform Position. &#160; </td><td class="markdownTableBodyNone"><a class="el" href="classlottie_1_1objects_1_1helpers_1_1Transform.html#a78772fcc2422407b99f6268337e1e4e9">position</a>  </td></tr>
<tr class="markdownTableRowOdd">
<td class="markdownTableBodyNone">s </td><td class="markdownTableBodyNone"><a href="#lottie_MultiDimensional">MultiDimensional</a> </td><td class="markdownTableBodyNone">Transform Scale. &#160; </td><td class="markdownTableBodyNone"><a class="el" href="classlottie_1_1objects_1_1helpers_1_1Transform.html#a6d8ee83d5c8586af48b4179f6c570537">scale</a>  </td></tr>
<tr class="markdownTableRowEven">
<td class="markdownTableBodyNone">r </td><td class="markdownTableBodyNone"><a href="#lottie_Value">Value</a> </td><td class="markdownTableBodyNone">Transform Rotation. &#160; </td><td class="markdownTableBodyNone"><a class="el" href="classlottie_1_1objects_1_1helpers_1_1Transform.html#aaf44bf742ef4b781a96cf5e138a6bc85">rotation</a>  </td></tr>
<tr class="markdownTableRowOdd">
<td class="markdownTableBodyNone">o </td><td class="markdownTableBodyNone"><a href="#lottie_Value">Value</a> </td><td class="markdownTableBodyNone">Transform Opacity. &#160; </td><td class="markdownTableBodyNone"><a class="el" href="classlottie_1_1objects_1_1helpers_1_1Transform.html#a7ad712c5dc892d97af430db97038ba37">opacity</a>  </td></tr>
<tr class="markdownTableRowEven">
<td class="markdownTableBodyNone">sk </td><td class="markdownTableBodyNone"><a href="#lottie_Value">Value</a> </td><td class="markdownTableBodyNone">Transform Skew. &#160; </td><td class="markdownTableBodyNone"><a class="el" href="classlottie_1_1objects_1_1helpers_1_1Transform.html#a81e3be7041809e2ee232797ed7778f37">skew</a>  </td></tr>
<tr class="markdownTableRowOdd">
<td class="markdownTableBodyNone">sa </td><td class="markdownTableBodyNone"><a href="#lottie_Value">Value</a> </td><td class="markdownTableBodyNone">Transform Skew Axis. &#160; </td><td class="markdownTableBodyNone"><a class="el" href="classlottie_1_1objects_1_1helpers_1_1Transform.html#a0487069c915c9133a5f8d4fe02759f74">skew_axis</a>  </td></tr>
</table>

## MultiDimensional
<table class="markdownTable">
<tr class="markdownTableHead">
<th class="markdownTableHeadNone">Lottie name </th><th class="markdownTableHeadNone">Type </th><th class="markdownTableHeadNone">Description </th><th class="markdownTableHeadNone">Attribute  </th></tr>
<tr class="markdownTableRowOdd">
<td class="markdownTableBodyNone">k </td><td class="markdownTableBodyNone">list of float </td><td class="markdownTableBodyNone">Non-animated value. &#160; </td><td class="markdownTableBodyNone"><a class="el" href="classlottie_1_1objects_1_1properties_1_1AnimatableMixin.html#a267dc4ad6263fafdd2e31c89cc7c4677">value</a>  </td></tr>
<tr class="markdownTableRowEven">
<td class="markdownTableBodyNone">ix </td><td class="markdownTableBodyNone">int </td><td class="markdownTableBodyNone">Property index. &#160; </td><td class="markdownTableBodyNone"><a class="el" href="classlottie_1_1objects_1_1properties_1_1AnimatableMixin.html#abd3692ba900a5521f56c169a9ee0ce48">property_index</a>  </td></tr>
<tr class="markdownTableRowOdd">
<td class="markdownTableBodyNone">a </td><td class="markdownTableBodyNone">0-1 int </td><td class="markdownTableBodyNone">Whether it's animated. &#160; </td><td class="markdownTableBodyNone"><a class="el" href="classlottie_1_1objects_1_1properties_1_1AnimatableMixin.html#a89dc4d6ab6311ec053ff263e01f41ff8">animated</a>  </td></tr>
<tr class="markdownTableRowEven">
<td class="markdownTableBodyNone">k </td><td class="markdownTableBodyNone">list of <a href="#lottie_OffsetKeyframe">OffsetKeyframe</a> </td><td class="markdownTableBodyNone">Keyframe list. &#160; </td><td class="markdownTableBodyNone"><a class="el" href="classlottie_1_1objects_1_1properties_1_1AnimatableMixin.html#a6dd560cb8d1b61a6c1a6b3af93a1ed55">keyframes</a>  </td></tr>
</table>

## For more properties

### Find the full list of properties [here](http://mattbas.gitlab.io/python-lottie/group__Lottie.html)
--

keywords: Lottie json, lottie structure,lottie json format, lottie json edit

---
title: AI绘图中遇到的问题
date: 2023-07-11 15:10:39
tags: [AI]
categories: 
---
# *复刻抽出来的图像会有细节偏差*
当使用青龙的wildcards插件抽卡时，只要使用hires.fix后生出来的图，就无法复刻
尝试过关闭xf、关闭其他插件只保留wildcards以及关闭xf并使用sdp进行出图均出现这种细节偏差

以下为两组对比
这张为wildcards+hires.fix出的原图
![](https://tenicol.oss-cn-shanghai.aliyuncs.com/website/202307111549401.png)
以下为参数：
(((masterpiece))),(((best quality))),(((extremely detailed))),(book cover \(medium\):1.4),(color connection:1.3),(stereogram:1.2),collage,\\n1girl,solo,\\nblue eyes, long hair, white hair, bangs, jewelry, ponytail, hair between eyes, hair ornament,\\\\nblack skirt, frilled skirt, frills,long sleeves,black pantyhose, white shirt,bow
Negative prompt: nsfw,duplicate, ugly, huge eyes, text, logo, worst face, (bad and mutated hands:1.3), (worst quality:2.0), (low quality:2.0), (blurry:2.0), horror, geometry, (bad hands), (missing fingers), multiple limbs, bad anatomy, (interlocked fingers:1.2), Ugly Fingers, (extra digit and hands and fingers and legs and arms:1.4), (deformed fingers:1.2), (long fingers:1.2),succubus wings,horn,succubus horn,succubus hairstyle,
Steps: 30, Sampler: DPM++ 2M Karras, CFG scale: 7, Seed: 3492162591, Size: 512x768, Model hash: 830984b8e1, Model: DarkMoon, Denoising strength: 0.58, Clip skip: 2, Wildcard prompt: "(((masterpiece))),(((best quality))),(((extremely detailed))),(__构图-画风__:1.4),(__色彩__:1.3),(__构图-效果__:1.2),__构图-构图方式__,\\\\n1girl,solo,\\\\nblue eyes, long hair, white hair, bangs, jewelry, ponytail, hair between eyes, hair ornament,\\\\\\\\nblack skirt, frilled skirt, frills,long sleeves,black pantyhose, white shirt,bow", Hires upscale: 2, Hires steps: 10, Hires upscaler: R-ESRGAN 4x+ Anime6B
这张为使用pnginfo发送到文生图进行生成的原图
![](https://tenicol.oss-cn-shanghai.aliyuncs.com/website/202307111549143.png)
参数：
(((masterpiece))),(((best quality))),(((extremely detailed))),(book cover \(medium\):1.4),(color connection:1.3),(stereogram:1.2),collage,\\n1girl,solo,\\nblue eyes, long hair, white hair, bangs, jewelry, ponytail, hair between eyes, hair ornament,\\\\nblack skirt, frilled skirt, frills,long sleeves,black pantyhose, white shirt,bow
Negative prompt: nsfw,duplicate, ugly, huge eyes, text, logo, worst face, (bad and mutated hands:1.3), (worst quality:2.0), (low quality:2.0), (blurry:2.0), horror, geometry, (bad hands), (missing fingers), multiple limbs, bad anatomy, (interlocked fingers:1.2), Ugly Fingers, (extra digit and hands and fingers and legs and arms:1.4), (deformed fingers:1.2), (long fingers:1.2),succubus wings,horn,succubus horn,succubus hairstyle,
Steps: 30, Sampler: DPM++ 2M Karras, CFG scale: 7, Seed: 3492162591, Size: 512x768, Model hash: 830984b8e1, Model: DarkMoon, Denoising strength: 0.58, Clip skip: 2, Hires upscale: 2, Hires steps: 10, Hires upscaler: R-ESRGAN 4x+ Anime6B

这一组为使用wildcards但不使用hires.fix出的图
![](https://tenicol.oss-cn-shanghai.aliyuncs.com/website/202307111552133.png)
参数：
(((masterpiece))),(((best quality))),(((extremely detailed))),(fourth wall:1.4),(aqua theme:1.3),(jpeg artifacts:1.2),feet out of frame,\\n1girl,solo,\\nblue eyes, long hair, white hair, bangs, jewelry, ponytail, hair between eyes, hair ornament,\\\\nblack skirt, frilled skirt, frills,long sleeves,black pantyhose, white shirt,bow
Negative prompt: nsfw,duplicate, ugly, huge eyes, text, logo, worst face, (bad and mutated hands:1.3), (worst quality:2.0), (low quality:2.0), (blurry:2.0), horror, geometry, (bad hands), (missing fingers), multiple limbs, bad anatomy, (interlocked fingers:1.2), Ugly Fingers, (extra digit and hands and fingers and legs and arms:1.4), (deformed fingers:1.2), (long fingers:1.2),succubus wings,horn,succubus horn,succubus hairstyle,
Steps: 30, Sampler: DPM++ 2M Karras, CFG scale: 7, Seed: 2193722990, Size: 512x768, Model hash: 830984b8e1, Model: DarkMoon, Clip skip: 2, Wildcard prompt: "(((masterpiece))),(((best quality))),(((extremely detailed))),(__构图-画风__:1.4),(__色彩__:1.3),(__构图-效果__:1.2),__构图-构图方式__,\\\\n1girl,solo,\\\\nblue eyes, long hair, white hair, bangs, jewelry, ponytail, hair between eyes, hair ornament,\\\\\\\\nblack skirt, frilled skirt, frills,long sleeves,black pantyhose, white shirt,bow"

![](https://tenicol.oss-cn-shanghai.aliyuncs.com/website/202307111553946.png)
参数：
(((masterpiece))),(((best quality))),(((extremely detailed))),(fourth wall:1.4),(aqua theme:1.3),(jpeg artifacts:1.2),feet out of frame,\\n1girl,solo,\\nblue eyes, long hair, white hair, bangs, jewelry, ponytail, hair between eyes, hair ornament,\\\\nblack skirt, frilled skirt, frills,long sleeves,black pantyhose, white shirt,bow
Negative prompt: nsfw,duplicate, ugly, huge eyes, text, logo, worst face, (bad and mutated hands:1.3), (worst quality:2.0), (low quality:2.0), (blurry:2.0), horror, geometry, (bad hands), (missing fingers), multiple limbs, bad anatomy, (interlocked fingers:1.2), Ugly Fingers, (extra digit and hands and fingers and legs and arms:1.4), (deformed fingers:1.2), (long fingers:1.2),succubus wings,horn,succubus horn,succubus hairstyle,
Steps: 30, Sampler: DPM++ 2M Karras, CFG scale: 7, Seed: 2193722990, Size: 512x768, Model hash: 830984b8e1, Model: DarkMoon, Clip skip: 2


# wav2lip_hq_trt
这是一个在原始wav2lip上，使用wav2lip、gfpgan、yolov5等模型用RT加速的超快推理！经测试在2070显卡上可达到0.03秒每帧实现实时推理。

【前言】

这是一个悲哀的故事，在训练wav2lip后发现嘴部很模糊，然后尝试使用gfpgan进行高清处理，讲实话训练wav2lip后的高清化效果是非常好的！然而推理速度是相当拉胯的，无法做到实时直播甚至实现类似“阿凡达模式”。至此推理上抛弃了face_detection，改用yolov5-trt。wav2lip和gfpgan全部改用trt。也就是整个推理项目弃用pytorch，改用trt加速。目前项目已经实现了，但是很悲哀，该项目并没有得到他人的认可和重用。这可悲的资本世界！！！

至此打算开源于此造福世界。

——一码超人


【效果】

实时效果：【速度1比0.6，高清】 https://www.bilibili.com/video/BV1Bu4y1y7MG/?share_source=copy_web&vd_source=5fa766cf0a6856c1ffa6536f1ebc6095

阿凡达模式：【阿凡达模式】 https://www.bilibili.com/video/BV1cK4y1w77r/?share_source=copy_web&vd_source=5fa766cf0a6856c1ffa6536f1ebc6095

自己:

https://github.com/oneCodeSuperman/wav2lip_hq_trt/assets/147574712/819db64b-1fb6-4035-a42a-d3c700da0666




【推理2070显卡】

初步的人脸分割速度：

![1](https://github.com/oneCodeSuperman/wav2lip_hq_trt/assets/147574712/da956bad-0c49-4659-97f9-af2da39845ab)

唇形+gfpgan单线程推理速度：

![2](https://github.com/oneCodeSuperman/wav2lip_hq_trt/assets/147574712/41c932d6-4616-4f02-90c9-ddf6c206f92d)

唇形+gfpgan三线程推理速度：

![3](https://github.com/oneCodeSuperman/wav2lip_hq_trt/assets/147574712/1740d294-7e3b-40f1-8bc9-ef239896ab6b)

即，时间/3等于单帧处理时间，如图0.09/3就是单帧推理0.03秒！

【最后的挣扎】

请允许我提倡最后的挣扎，如有意拿下该项目可联系本人微信，在此将不公开源代码。
个人微信:yanghao19960301

最后开源期限暂定。

![5d8e2e27-c6a6-48d4-bd0a-9e6398c8b266](https://github.com/oneCodeSuperman/wav2lip_hq_trt/assets/147574712/1d8b0696-ecc0-42e7-85f0-563158a02e8d)




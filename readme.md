## ComposedImage
有一天我看见一张图,那个图我弄没了,大意就是一张滑稽，但是是由许多黄黄的小黄图拼起来的。我想了想，好像也不难做啊，就用OpenCV写了一个功能类似的。
效果图如下：
![](https://github.com/CaomingatUESTC/ComposeImage/raw/master/example.png)

我用于合成的图片是最近看的日番《野良神》里男主角夜斗，用了大概十张图作为原始素材，然后就是重复用这十张图。问题在于夜斗吧，他大部分靓照都是深色背景，头发也是黑的，然后出来的结果就暗一点。我看到的那个滑稽嘛，小黄图，黄黄的，比较贴近滑稽的颜色，效果就好一点。

原理就是把用于拼接的图等比例缩小到宽度为10个像素，然后求得输入的图像对应位置ROI的平均像素值，然后给拼接图加上这个像素值（当然实际操作复杂点，不是直接加就可以），然后就出来了。

这个程序用法大概是这样的。

./ComposeImage '你想得到的图的原始图' '你想用于拼接的图的文件夹'

祝大家玩的愉快。


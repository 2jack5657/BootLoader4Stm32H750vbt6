本仓库用于存放针对正点原子MiniPro H750开发板编写的用于Clion+Openocd调试的BootLoader和Application工程模板

使用正点原子提供的flash驱动，支持全系列华邦的norflash芯片。正点原子MiniPro H750开发板出厂自带的芯片是By25q128，理论上也能用，但是openocd不支持博雅的flash，因此需要先确定自己的Flash的型号然后自行更换。

这个Clion+Openocd的开发方式其实在linux上更好用，我在windows上使用只是因为用keil5用烦了而已（。

使用方法：先烧录Bootloader，然后复位，当红灯亮起时能自由对flash(无论内部外部)自由烧写，此时可以切换到app工程烧录至外部flash中，烧录完成后按下开发板上的Wk_UP按键即可跳转至应用程序。跳转之后红灯熄灭。

这个Bootloader花了我大概1个多月的时间吧，期间参考了许多的帖子和工程，看了看他们的思路，感觉许多人的思路都对，就是实现的过程复杂了点，本工程采用了一种取巧的思路吧。

顺带一提，这一个多月有一半的时间都在和博雅以及openocd作斗争，要不是我去翻了翻openocd的源码，我可能到现在还不会知道原来openocd不支持博雅的flash...

在更换flash的过程中由于没有风枪还把flash的焊盘搞下来了，还好我技高一筹，补了回去，差点喜提废板一块...

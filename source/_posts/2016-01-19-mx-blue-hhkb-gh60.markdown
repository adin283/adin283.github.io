---
layout: post
title: "MX Blue HHKB GH60"
date: 2016-01-18 23:35:24 +0800
comments: true
categories: 
---
{% img /images/GH60/GH60_light_full.JPG 'GH60_light_full.JPG' 'GH60_light_full.JPG' %}

一直是一把 HHKB Pro2 在公司使用，回家的话就用 mpb 自带的键盘。
期间也用过青轴 minila air、poker2，但是 minila air 右边 shift 比较蛋疼，而且空格键很短，左边经常按不到，虽然左边的 fn 是可以设置成空格的，但是按着还是挺不爽的；poker2没有用很长时间，但是用过了 hhkb 之后就受不鸟其他键位了。。。所以一直都是用 mbp 的自带薄膜键盘，用 Karabiner 映射了一些键，比如 | 改成 delete。
## 突发奇想
要是能有一把 HHKB 键位的青轴键盘就好了，因为之前用过几把机械键盘都是青轴的，还是对青轴比较情有独钟一些。后来也去试过 minila air 和 cherry 的红轴，感觉和 hhkb pro2 手感其实相差不多，所以还是决定组一个青轴的区别与 hhkb pro2 的手感。
## 搜索材料
首先了解了一下板子，santa 的电路板我看了下，是可以组成 hhkb 键位的。于是当晚拉着客服问到了两点多，就下单了。
清单如下：

	1. santa pcb 板子
	2. 定位板/钢板
	3. 卫星轴 4 个（空格，shift * 2，enter，control/caps lock）
	4. cherry青轴 67 个（老板给多发了几个，因为青轴可能有些坏轴）
	5. 塑料外壳
	6. PBT 键帽 117 键的，键位刚好组 hhkb 的键位
	7. 轴间纸一张
	8. 透明轴盖 65 个
	9. 热插拔针脚 130 个（一个键帽两个脚）
## 组装步骤
### 组装卫星轴
有防呆设计，直接装上就好了，卡进的时候可能要稍稍用点力，没事不会弄坏，黑色的塑料还是有一些韧性的。组装好卫星轴后安装到 PCB 板上，有卡扣按上就好了。
### 开轴改热插拔，上轴间纸
开轴盖其实很简单，用镊子就可以，我刚开始在公司没有镊子，找了两个牙签开的也挺轻松。轴盖打开之后把两个热插拔针脚插入轴上方 LED 针脚处，然后贴上轴间纸，再盖上透明轴盖。这步挺费工夫的，我搞了两三个小时才搞定。其实吧，热插拔和轴间纸都没有必要装；反正 LED 便宜，真的要幻灯把 LED 换了就是。轴间纸也是玄学，根本不能防尘和影响手感。透明轴盖除了装B也没有什么乱用。
### 固定轴到 PCB 和定位板
层次结构是这样的：PCB，轴，定位板。这步有点技巧，把四周的轴先安装好，然后再安装中间的轴。不要先把轴都卡好在定位板上，这样你会发现怎么都没法插到 PCB 板上了，因为 PCB 板上的 LED 孔很小，很难对上。而且现在是一个轴4个脚，你要一下将60 * 4，就是240个脚同时对准插在 PCB 板上，难度可想而知。所以如果你觉得定位板对手感影响不大的话，就可以省掉定位板，这样安装轴的难度会小很多。安装轴的时候注意不要将轴上的针脚弄歪，这样针脚容易折掉，没有插到 PCB 上对应的空里，需要拔下来重新插过。按好再拔下来难度很大。
要注意的是，拿你的键帽笔画一些，轴不要按错位置，不然后面你会发现怎么键帽相互打架，就悲剧了。这个事情在撸主身上就发生了，坐下的三个键，我往右边偏了一格，结果三个键全都拆下来重新按，重新焊；还好有吸枪，还是拆下来了。反正就是拆比装难了，一定不要按错了。
### 焊接
用橡皮筋固定PCB，轴和定位板，然后就上焊锡、松香电烙铁焊吧。最好弄个可调温的电烙铁，温度设置在400度比较合适。我是焊一排然后插到电脑上测试一排，如果有问题可以及时修正。240多个脚，加油焊吧，其实焊接还是挺快的，最费时费力的还是开轴改热插拔和贴轴间纸那步，所以我强烈建议不用改热插拔和贴轴间纸。
{% img /images/GH60/GH60_weld_1.JPG 'GH60_weld_1.JPG' 'GH60_weld_1.JPG' %}
{% img /images/GH60/GH60_weld_2.JPG 'GH60_weld_2.JPG' 'GH60_weld_2.JPG' %}
### 测试键位
再测试一下所有键是否有用，右上角的键因为没有刷配系的原因可能是么有用的，没有关系你用万用表蜂鸣档试下，按键按下的时候能通就没有问题。一会刷了配系就好了。
### 安装热插拔 LED
LED 灯脚需要剪一下，剪了之后插进热插拔的孔就好，注意下正负极。默认是 fn + v，打开键盘灯，在打开键盘灯的情况下安装灯吧，安上点亮就好了，正负极安反也没关系，不会烧掉的。换下正负极就是了。
LED 长角的是正极，但是你剪短之后两个脚是一样长的，怎么区分正负极呢，你看 LED 等里面那坨东西有两部分组成，比较小一点的那个是正极。全按上之后就都亮了，恩，完美。
{% img /images/GH60/GH60_LED.JPG 'GH60_LED.JPG' 'GH60_LED.JPG' %}
### 安装外壳
把焊好的 PCB 安装到外壳上，有6颗螺丝，拧上就好了。
### 安装键帽
键帽高度从下到上是 R1，R1，R2，R3，R4。一个个按上就是了，有卫星轴的对准一下卫星轴。那么硬件部分就组装好了。
### 刷配系/固件
mac 上据我所知只能刷 hex，有两个[tmk_keyboard](https://github.com/tmk/tmk_keyboard)，[tmk_keyboard_custom](https://github.com/kairyu/tmk_keyboard_custom)。记得是刷[tmk_keyboard_custom](https://github.com/kairyu/tmk_keyboard_custom),不要去刷tmk_keyboard那个，刷了tmk_keyboard之后可能导致键盘没有反应，我也不知道为什么。
```
//mac上需要安装的编译环境
brew install Caskroom/cask/crosspack-avr
brew install gcc-avr
brew install dfu-programmer
brew install gcc
```
再说一遍，请用[tmk_keyboard_custom](https://github.com/kairyu/tmk_keyboard_custom)
在keyboard/gh60/config.h中定义宏 #define GH60_REV_CHN 1
make KEYMAP=hhkb dfu
但是你会发现有些报错，我一个个解决了，但是刷好之后，键盘并不能达到我想要的配系。所以我还是回家用 windows 的机器来刷 epp 文件，这个是图形化的工具比较简单。
项目地址：[tkg-toolkit](https://github.com/kairyu/tkg-toolkit)
图形化界面网址：
[keyboard-layout-editor](http://www.keyboard-layout-editor.com/#/gists/bd039cbcf89e7fad09e8)
[tkg](http://www.enjoyclick.org/tkg/)
编辑好键位之后复制 raw-data 的 json 数据，粘贴的 tkg 网站里面，生成 epp。
然后设置tkg-toolkit/windows/setup.bat来安装设置，用tkg-toolkit/windows/reflash.bat来刷固件，刷之前按一下键盘背后的按钮进入 dfu 模式。如果有问题，记得装键盘驱动。

## 成品图
{% img /images/GH60/GH60_light_gray.JPG 'GH60_light_gray.JPG' 'GH60_light_gray.JPG' %}
{% img /images/GH60/GH60_light_part.JPG 'GH60_light_part.JPG' 'GH60_light_part.JPG' %}
{% img /images/GH60/GH60_no_light.JPG 'GH60_no_light.JPG' 'GH60_no_light.JPG' %}

## 参考链接：
* [satan版GH 60组有钢茶 POKER配列详细教程](http://www.pcwaishe.cn/thread-632487-1-1.html)
* [tkg](http://www.enjoyclick.org/tkg/)
* [keyboard-layout-editor](http://www.keyboard-layout-editor.com/)
* [GH60PCB对比之Satan & 菜菜](http://www.satan.com.cn/p/399.html)
* [ 新手扫盲——《GH60》 ](http://pcwaishe.cn/thread-641592-1-1.html)
* [【你真的了解“轴间纸”？会装吗？内附详细教程】](http://www.pcwaishe.cn/thread-540703-1-1.html)
* [機械式鍵盤60Key-GH60 刷鍵位教程](http://www.armygroup.com.tw/sns/space.php?do=thread&id=54&uid=23227)
* [拿到 GH60 的艰辛与幸福之路](http://www.v2ex.com/t/161887)
* [刷配系视频](http://yuntv.letv.com/bcloud.html?uu=7ddc155d09&vu=b90507659c)
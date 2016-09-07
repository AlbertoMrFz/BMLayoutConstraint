<p align="center">
<img src="http://beichenming.me/img/BMLayoutConstraint_logo.jpg" alt="BMLayoutConstraint" title="BMLayoutConstraint" width="557"/>
</p>

<p align="center">
<a href="http://beichenming.me"><img src="https://img.shields.io/badge/Blog-@%E5%8C%97%E8%BE%B0%E6%98%8E-red.svg?style=flat"></a>
</p>

BMLayoutConstraint是一套UI布局适配工具，通过JSON配置文件的形式能够快速适配不同设备以及多语言下的UI布局差异，适用于iOS以及Mac OSX应用程序的开发，通过Object-C编写。

BMLayoutConstraint还在不断完善中，欢迎大家一起。

## 运行环境

- iOS 8+
- Xcode 6+

## 示例
使用BMLayoutConstraint的前提是我们的UI布局采用的是Mansory或者其他纯代码布局的方式，BMLayoutConstraint并不适合xib或者storyboard这种形式的布局方式，我们已Demo为例进行使用说明。

第一步：
我们需要在工程下建立存放配置文件的目录，我们新建四个目录来对应我们的设备类型：
<p align="left">
<img src="device_dir.jpg" alt="BMLayoutConstraint" title="BMLayoutConstraint" width="300"/>
</p>

drawable-iPad(768 * 1024)

drawable-iPhone5_S_C_SE(320 * 568)

drawable-iPhone6_S(375 * 667)

drawable-iPhone6P_S(414 * 736)

因为iPad的尺寸比较多，所以我们目前使用了一个通用的尺寸表示，未来会继续扩展。

第二步:
针对需要适配的界面，建立对应名字的适配文件，例如我们要对ViewController中的元素布局进行适配就需要建立四个ViewController的json配置文件并以设备名结尾。

json配置文件的格式如下，我们已iPhone6为例：

```
 "UILabel" :
 [
      {
          "bm_ViewControllerPhoneNoLabelID_BM_ZH_HANS_US" :
          {
              "marginLeft" : 30.0,
              "marginRight" : 0.0,
              "marginTop" : 100.0,
              "marginBottom" : 0.0,
              "width" : 100.0,
              "height" : 20.0,
              "fontSize" : 16.0
          }
      },
      {
          "bm_ViewControllerPhoneNoLabelID_BM_EN_US" :
          {
              "marginLeft" : 30.0,
              "marginRight" : 0.0,
              "marginTop" : 100.0,
              "marginBottom" : 0.0,
              "width" : 150.0,
              "height" : 20.0,
              "fontSize" : 16.0
          }
      },
   ]

```
每一个控件都有自己的唯一ID


## 博客
[My Blog](http://www.jianshu.com/users/5d1e6bd11aa0)

## 语言
[中文说明]()


# Sdvx controller 

# 材料清单
1.购买stm32f103c8t6最小核心板 
2.购买烧录工具如 stlink（推荐），jlink        
3.360ppr的编码器或者其他线数的编码器 两个 
4.sdvx按键
5.微动开关，霍尼韦尔v15s05-ez025-k02，欧姆龙的也可以，需购买7个
6.xh2.54端子，2p x7 4p x2（建议多买不贵，端子容易焊坏），其他连接器也可，也可以飞线  
7.购买xh2.54的连接线同 2p和4p的连接线  价格和6中的端子加起来一个十块左右
8.切割亚克力面板 
9.购买木盒。
预估成本
# 代码烧录以及接线顺序  
下载解压压缩包  
![Image](https://user-images.githubusercontent.com/105113020/266985680-279d3b45-5d15-4137-8ac3-d55ff37bda7d.png)   
引脚对应  
PA0 左编码器A相  
PA1 左编码器B相  
PA2 BT-A  
PA3 BT-B  
PA4 BT-C  
PA5 BT-D  
PA6 右编码器A相  
PA7 右编码器B相  
PB0 FX-L  
PB1 FX-R  
PB10 START  
使用stlink 或者jlink，打开工程文件(提前提前安装好mdk-arm)，选择调试设备并勾选调试模式为swd，swdio与swdclk对应引脚连接。  
也可以烧录hex文件，准备ch340，改为bootloader启动，使用isp烧录。  
下载整个压缩包即可，代码烧录部分可以百度stm32f103代码烧录方法，文件工程在压缩文件中，代码烧录完成后可以将端子的两个引脚短接一下看看电脑输入法是否有相应的反应，旋钮引脚由于悬空的原因，在未连线的情况下鼠标可能会乱跳属于正常现象，连接后即可正常使用，代码烧录完成基本就大功告成。
pcb部分在末尾，建议使用第一个核心板版本（目前文件只有第一个版本，后面那个大多数人不会用还很麻烦所以就不传了），嘉立创免费打板，百度搜索一下立创eda，打开工程文件可以查看板子原理图和pcb，搜索嘉立创每月领券打板两次即可白嫖，拿到板子后只有排母和xh座子需要焊接非常容易，编码器和按键微动开关的线焊接需要注意（微动开关焊接常开两个引脚）
淘宝买2p和4p的线和端子，2p用于按键不分方向只起到引脚和gnd导通的作用，4p用于编码器，一定要注意方向，编码器上面vcc和信号线颜色都有说明不要接反了，检查无误后再插电否则接反编码器容易烧毁
![image](https://github.com/mozhemoqi/sdvx-controller-based-on-stm32/assets/105113020/5d954a20-3bc7-4674-b702-8b4f821df375)

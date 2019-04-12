# PAOGD_HW2
## 介绍
PAOGD个人作业2-角色动画基础

## 开发环境
Blender2.8 beta

## DeadLine: 4月12日 22 点
## 场景描述
实现一个简单的行走循环动画

![walk](https://github.com/maozhimo/POAGD/blob/master/image%20sec/HW2.gif?raw=true)

## Tips
导入模型,得到角色网格（根目录下的stickman.obj或其他模型，可自己构造，在report中说明）
在角色网格的基础上创建基础骨架(Armature)

![daoru](https://gitee.com/uploads/images/2019/0404/155350_38fd066f_1194012.png)
快捷键e在根节点拉伸，shift加e对称x轴拉伸

![lashenxinjian](https://github.com/maozhimo/POAGD/blob/master/image%20sec/QQ%E5%9B%BE%E7%89%8720190412142642.png?raw=true)
主干骨与胳膊和腿断开父子关系

![duankai](https://github.com/maozhimo/POAGD/blob/master/image%20sec/QQ%E5%9B%BE%E7%89%8720190412142731.png?raw=true)

## 为骨架添加约束器,利用反向运动学(Inverse Kinematics)实现腿部装配
添加小腿的ik约束，由脚提供，权重为2

![ik](https://github.com/maozhimo/POAGD/blob/master/image%20sec/QQ%E5%9B%BE%E7%89%8720190412143820.png?raw=true)
添加膝盖大腿的ik约束，权重为1

![ik](https://github.com/maozhimo/POAGD/blob/master/image%20sec/QQ%E5%9B%BE%E7%89%8720190412143816.png?raw=true)
## 进入权重绘制(Weight Paint)模式修改顶点权重
选中人物和骨架自动配置权重

![huizhi](https://github.com/maozhimo/POAGD/blob/master/image%20sec/QQ%E5%9B%BE%E7%89%8720190412144516.png?raw=true)
笔刷更改

![huizhi](https://github.com/maozhimo/POAGD/blob/master/image%20sec/QQ%E5%9B%BE%E7%89%8720190412144215.png?raw=true)
## 在动作编辑器(Action Editor)模式创建行走动作
添加5帧动作

![huizhi](https://github.com/maozhimo/POAGD/blob/master/image%20sec/W7%25Q0@%25PQB9FO@U@8D~CGN9.png?raw=true)
### 开始做的时候没有断开脚和小腿的父子关系，所以最后做出来动作，腿一直在颤抖。
## 利用姿态镜像使创建的动作可循环
在NonLinear Animation模式下重复Walk动作

![huizhi](https://github.com/maozhimo/POAGD/blob/master/image%20sec/IJY2145DC~QG$2IO%5DRLLNI4.png?raw=true)
![huizhi](https://github.com/maozhimo/POAGD/blob/master/image%20sec/JK_XP%7B0M$0JN$DAI_~FUKUW.png?raw=true)

添加曲线,并让小人沿着曲线行走
我是绑定坐标系进行移动的，其实也可以让坐标系跟随曲线移动。

![bamgding](https://github.com/maozhimo/POAGD/blob/master/image%20sec/L@4M3G4TRK7_EL2Y9@7RRN7.png?raw=true)
![bangding](https://github.com/maozhimo/POAGD/blob/master/image%20sec/QQ%E6%88%AA%E5%9B%BE20190412145629.png?raw=true)

## 不过因为后面做出来动画有点像溜冰，是帧数间隔过大，坐标系移动的太多的问题，但感觉很有意思就不想改了。虽然有些要求没达到，但我基本已经掌握了操作。
## 做的蛮开心的，动作很有趣哈哈
合理地摆放、控制镜头

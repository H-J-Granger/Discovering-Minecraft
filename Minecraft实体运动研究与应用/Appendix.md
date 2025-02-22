## 附录A常见实体运动属性

下面总结一些常见的实体的运动相关属性，其中运算顺序含义见3.1节，A为重力之外的某种加速。为了方便实际应用，这里给出的是实体的速度乘数，也就是公式中用到的"k"，阻力系数并未直接给出。

> 表A1常见实体运动属性表

| 实体                          | 重力/($m/gt^2$) | 速度乘数（k值） | 高度/m | 宽度/m | 眼部高度/m | 运算顺序 |
|------|-------|------|------|------|------|------|
| TNT                           | 0.04               | 0.98            | 0.98   | 0.98   | 0.15       | GMD      |
| 下落的方块                    | 0.04               | 0.98            | 0.98   | 0.98   | 0.833      | GMD      |
| 空中的物品                    | 0.04               | 0.98***(1)*** | 0.25   | 0.25   | 0.2125     | GMD      |
| 空中的经验球                  | 0.03               | 0.98***(2)*** | 0.5    | 0.5    | 0.425      | GMD      |
| 空中的船                      | 0.04               | 水平0.9，Y轴1   | 0.5625 | 1.375  | 0.5625     | GDM      |
| 空中的矿车                    | 0.04               | 0.95            | 0.7    | 0.98   | 0.595      | GMD      |
| 空中的箭矢/三叉戟             | 0.05***(3)*** | 0.99***(3)*** | 0.5    | 0.5    | 0.13       | MDG      |
| 空中的雪球/鸡蛋/末影珍珠      | 0.03***(3)*** | 0.99***(3)*** | 0.25   | 0.25   | 0.2125     | MDG      |
| 空中的药水瓶                  | 0.05***(3)*** | 0.99***(3)*** | 0.25   | 0.25   | 0.2125     | MDG      |
| 空中的附魔之瓶                | 0.07***(3)*** | 0.99***(3)*** | 0.25   | 0.25   | 0.2125     | MDG      |
| 空中的恶魂和末影龙火球        | 0                  | 0.95***(3)*** | 1      | 1      | 0.85       | MAD      |
| 空中的烈焰人火球/普通凋零之首 | 0         | 0.95***(3)*** | 0.3125 | 0.3125 | 0.265625   | MAD      |
| 空中的鱼竿浮标     | 0.03               | 0.92            | 0.25   | 0.25   | 0.2125     | GMD      |
| 空中的蓝色凋零之首            | 0                  | 0.73(3)  | 0.3125 | 0.3125 | 0.265625   | MAD      |
| 空中的羊驼唾沫                | 0.06***(3)*** | 0.99***(3)*** | 0.25   | 0.25   | 0.2125     | MDG      |
| 无有效目标的潜影贝导弹  | 0.04               | 1               | 0.3125 | 0.3125 | 0.265625   | GM       |
| 空中或地面上的玩家（除体积和眼部高度外也适用于大部分生物和盔甲架） | 0.08               | 水平0.91***(3)***，Y轴0.98***(3)*** | 站立时1.8，睡觉和濒死时0.2，鞘翅飞行和游泳和激流飞行时0.6，潜行时1.5 | > 站立、潜行、鞘翅飞行和游泳和激流飞行时0.6，睡觉和濒死时0.2 | > 睡觉时为0.2，游泳、鞘翅飞行和激流飞行时为0.4，潜行时为1.27，站立时为1.62 |              |
| 水中的玩家（除体积和眼部高度外也适用于大部分生物和盔甲架）         | 0.005              | 水平取决于深海探索者等级，Y轴0.8***(3)***  同上 | 同上  |    | 同上       | MDG      |
| 较深熔岩中的玩家（除体积和眼部高度外也适用于大部分生物和盔甲架）   | 0.005              | 0.5| 同上| 同上 |   | 同上       |

(1)：如需高精度计算水平运动，建议X、Z轴上使用这里给出的数值的单精度浮点真实值，可在表2.5中找到

(2)：如需高精度计算竖直运动，建议Y轴上使用这里给出的数值的单精度浮点真实值，可在表2.5中找到

(3)：如需高精度计算竖直运动，建议使用这里给出的数值的单精度浮点真实值，部分可在表2.5中找到

## 附录B完整公式

这是第3节中部分公式对于不同实体类型的各种形式，除MDA类实体对应各式和求出$\Delta d_{n}$、$d_{n}$、$v_{0}$、$\Delta d_{\max}$和$d_{\max}$的各式以及"万能方程组"基本确定无误外，其它公式不排除仍存在推导错误或录入错误，但缺少检验方法，希望有人帮忙检查一下。

**MDA（移动-\>阻力-\>加速）**

$$\begin{matrix}
\Delta d_{n} = k^{n - 1}v_{0}t_{0} + \frac{a{t_{0}}^{2}\left( 1 - k^{n - 1} \right)}{1 - k}\#(B.1.1) \\
\end{matrix}$$

$$\begin{matrix}
d_{n} = \frac{v_{0}t_{0}\left( 1 - k^{n} \right)}{1 - k} + \frac{a{t_{0}}^{2}\left\lbrack k^{n} + n(1 - k) - 1 \right\rbrack}{(1 - k)^{2}}\#(B.1.2) \\
\end{matrix}$$

$$\begin{matrix}
v_{0} = \frac{d_{n}{t_{0}}^{- 1}(1 - k) - at_{0}n}{1 - k^{n}} + \frac{at_{0}}{1 - k}\#(B.1.3) \\
\end{matrix}$$

$$\begin{matrix}
n = - \log_{k}\left\lbrack \frac{1}{k} - \frac{v_{0}(1 - k)}{at_{0}k} \right\rbrack\#(B.1.4) \\
\end{matrix}$$

$$\begin{matrix}
\Delta d_{\max} = \frac{a{t_{0}}^{2}}{1 - k}\#(B.1.5) \\
\end{matrix}$$

$$\begin{matrix}
d_{\max} = \frac{v_{0}t_{0}}{1 - k}\#(B.1.6) \\
\end{matrix}$$

$$\begin{matrix}
{tan\alpha}_{n} = \frac{gt_{0}\left( k^{n - 1} - 1 \right)}{k^{n - 1}(1 - k)\sqrt{{v_{x0}}^{2} + {v_{z0}}^{2}}} - \frac{v_{y0}}{\sqrt{{v_{x0}}^{2} + {v_{z0}}^{2}}}\#(B.1.7) \\
\end{matrix}$$

$${y = \frac{v_{y}(1 - k) - gt_{0}}{v_{x0}(1 - k)}x - \frac{g{t_{0}}^{2}}{1 - k}\log_{k}\lbrack 1 - \frac{x(1 - k)}{v_{x0}t_{0}}\rbrack y
}\begin{matrix}
 = \frac{v_{y}(1 - k) - gt_{0}}{v_{z0}(1 - k)}z - \frac{g{t_{0}}^{2}}{1 - k}\log_{k}\left\lbrack 1 - \frac{z(1 - k)}{v_{z0}t_{0}} \right\rbrack\#(B.1.8) \\
\end{matrix}$$

$$\begin{matrix}
\tan\alpha\sqrt{{x_{n}}^{2} + {z_{n}}^{2}} = \frac{g{t_{0}}^{2}\left( 1 - k^{n} \right)}{(1 - k)^{2}} - \frac{g{t_{0}}^{2}n - v_{y0}^{'}t_{0}\left( 1 - k^{n} \right)}{1 - k} - y_{n}\#(B.1.9) \\
\end{matrix}$$

> **DMA（阻力-\>移动-\>加速）**

$$\begin{matrix}
\Delta d_{n} = k^{n}v_{0}t_{0} + \frac{a{t_{0}}^{2}\left( k - k^{n} \right)}{1 - k}\#(B.2.1) \\
\end{matrix}$$

$$\begin{matrix}
d_{n} = \frac{v_{0}t_{0}\left( k - k^{n + 1} \right)}{1 - k} + \frac{a{t_{0}}^{2}k\left\lbrack k^{n} + n(1 - k) - 1 \right\rbrack}{(1 - k)^{2}}\#(B.2.2) \\
\end{matrix}$$

$$\begin{matrix}
v_{0} = \frac{d_{n}{t_{0}}^{- 1}(1 - k) - at_{0}kn}{k - k^{n + 1}} + \frac{at_{0}}{1 - k}\#(B.2.3) \\
\end{matrix}$$

$$\begin{matrix}
n = - \log_{k}\left\lbrack \frac{1}{k} - \frac{v_{0}(1 - k)}{at_{0}k} \right\rbrack\#(B.2.4) \\
\end{matrix}$$

$$\begin{matrix}
\Delta d_{\max} = \frac{a{t_{0}}^{2}k}{1 - k}\#(B.2.5) \\
\end{matrix}$$

$$\begin{matrix}
d_{\max} = \frac{v_{0}t_{0}k}{1 - k}\#(B.2.6) \\
\end{matrix}$$

> **DAM（阻力-\>加速-\>移动）**

$$\begin{matrix}
\Delta d_{n} = k^{n}v_{0}t_{0} + \frac{a{t_{0}}^{2}\left( 1 - k^{n} \right)}{1 - k}\#(B.3.1) \\
\end{matrix}$$

$$\begin{matrix}
d_{n} = \frac{v_{0}t_{0}\left( k - k^{n + 1} \right)}{1 - k} + \frac{a{t_{0}}^{2}\left\lbrack k^{n + 1} + n(1 - k) - k \right\rbrack}{(1 - k)^{2}}\#(B.3.2) \\
\end{matrix}$$

$$\begin{matrix}
v_{0} = \frac{d_{n}{t_{0}}^{- 1}(1 - k) - at_{0}n}{k - k^{n + 1}} + \frac{at_{0}}{1 - k}\#(B.3.3) \\
\end{matrix}$$

$$\begin{matrix}
n = - \log_{k}\left\lbrack 1 - \frac{v_{0}(1 - k)}{at_{0}} \right\rbrack\#(B.3.4) \\
\end{matrix}$$

$$\begin{matrix}
\Delta d_{\max} = \frac{a{t_{0}}^{2}}{1 - k}\#(B.3.5) \\
\end{matrix}$$

$$\begin{matrix}
d_{\max} = \frac{v_{0}t_{0}k}{1 - k}\#(B.3.6) \\
\end{matrix}$$

> **MAD（移动-\>加速-\>阻力）**

$$\begin{matrix}
\Delta d_{n} = k^{n - 1}v_{0}t_{0} + \frac{a{t_{0}}^{2}\left( k - k^{n} \right)}{1 - k}\#(B.4.1) \\
\end{matrix}$$

$$\begin{matrix}
d_{n} = \frac{v_{0}t_{0}\left( 1 - k^{n} \right)}{1 - k} + \frac{a{t_{0}}^{2}k\left\lbrack k^{n} + n(1 - k) - 1 \right\rbrack}{(1 - k)^{2}}\#(B.4.2) \\
\end{matrix}$$

$$\begin{matrix}
v_{0} = \frac{d_{n}{t_{0}}^{- 1}(1 - k) - at_{0}kn}{1 - k^{n}} + \frac{at_{0}k}{1 - k}\#(B.4.3) \\
\end{matrix}$$

$$\begin{matrix}
n = - \log_{k}\left\lbrack \frac{1}{k} - \frac{v_{0}(1 - k)}{at_{0}k^{2}} \right\rbrack\#(B.4.4) \\
\end{matrix}$$

$$\begin{matrix}
\Delta d_{\max} = \frac{a{t_{0}}^{2}k}{1 - k}\#(B.4.5) \\
\end{matrix}$$

$$\begin{matrix}
d_{\max} = \frac{v_{0}t_{0}}{1 - k}\#(B.4.6) \\
\end{matrix}$$

> **AMD（加速-\>移动-\>阻力）**

$$\begin{matrix}
\Delta d_{n} = k^{n - 1}v_{0}t_{0} + \frac{a{t_{0}}^{2}\left( 1 - k^{n} \right)}{1 - k}\#(B.5.1) \\
\end{matrix}$$

$$\begin{matrix}
d_{n} = \frac{v_{0}t_{0}\left( 1 - k^{n} \right)}{1 - k} + \frac{a{t_{0}}^{2}\left\lbrack k^{n + 1} + n(1 - k) - k \right\rbrack}{(1 - k)^{2}}\#(B.5.2) \\
\end{matrix}$$

$$\begin{matrix}
v_{0} = \frac{d_{n}{t_{0}}^{- 1}(1 - k) - at_{0}n}{1 - k^{n}} + \frac{at_{0}k}{1 - k}\#(B.5.3) \\
\end{matrix}$$

$$\begin{matrix}
n = - \log_{k}\left\lbrack 1 - \frac{v_{0}(1 - k)}{at_{0}k} \right\rbrack\#(B.5.4) \\
\end{matrix}$$

$$\begin{matrix}
\Delta d_{\max} = \frac{a{t_{0}}^{2}}{1 - k}\#(B.5.5) \\
\end{matrix}$$

$$\begin{matrix}
d_{\max} = \frac{v_{0}t_{0}}{1 - k}\#(B.5.6) \\
\end{matrix}$$

$$\begin{matrix}
{tan\alpha}_{n} = \frac{gt_{0}\left( k^{n} - 1 \right)}{k^{n - 1}(1 - k)\sqrt{{v_{x0}}^{2} + {v_{z0}}^{2}}} - \frac{v_{y0}}{\sqrt{{v_{x0}}^{2} + {v_{z0}}^{2}}}\#(B.5.7) \\
\end{matrix}$$

$$\begin{matrix}
\tan\alpha\sqrt{{x_{n}}^{2} + {z_{n}}^{2}} = \frac{g{t_{0}}^{2}\left( k - k^{n + 1} \right)}{(1 - k)^{2}} - \frac{g{t_{0}}^{2}n - v_{y0}^{'}t_{0}\left( 1 - k^{n} \right)}{1 - k} - y_{n}\#(B.5.8) \\
\end{matrix}$$

> **ADM（加速-\>阻力-\>移动）**

$$\begin{matrix}
\Delta d_{n} = k^{n}v_{0}t_{0} + \frac{a{t_{0}}^{2}\left( k - k^{n + 1} \right)}{1 - k}\#(B.6.1) \\
\end{matrix}$$

$$\begin{matrix}
d_{n} = \frac{v_{0}t_{0}\left( k - k^{n + 1} \right)}{1 - k} + \frac{a{t_{0}}^{2}k\left\lbrack k^{n + 1} + n(1 - k) - k \right\rbrack}{(1 - k)^{2}}\#(B.6.2) \\
\end{matrix}$$

$$\begin{matrix}
v_{0} = \frac{d_{n}{t_{0}}^{- 1}(1 - k) - at_{0}kn}{k - k^{n + 1}} + \frac{at_{0}k}{1 - k}\#(B.6.3) \\
\end{matrix}$$

$$\begin{matrix}
n = - \log_{k}\left\lbrack 1 - \frac{v_{0}(1 - k)}{at_{0}k} \right\rbrack\#(B.6.4) \\
\end{matrix}$$

$$\begin{matrix}
\Delta d_{\max} = \frac{a{t_{0}}^{2}k}{1 - k}\#(B.6.5) \\
\end{matrix}$$

$$\begin{matrix}
d_{\max} = \frac{v_{0}t_{0}k}{1 - k}\#(B.6.6) \\
\end{matrix}$$

## 附录C研究环境及辅助性工具

大部分实验内容来自Minecraft Java版 1.16.4，极少部分来自Java版1.16.5的MCP，在1.16.4的实验中用到了以下辅助Mod：

(1) fabric-carpet-1.16.4-1.4.17+v201111

(2) mcwmem-1.16.4-20210714

(3) chunkmap-20210718

(4) malilib-fabric-1.16.4-0.10.0-dev.21+arne.1

(5) minihud-fabric-1.16.4-0.19.0-dev.20201103.184029

(6) tweakeroo-fabric-1.16.4-0.10.0-dev.20201110.132827

mcwmem全称为Minecraft World Manipulation Enchantment Mod（Minecraft世界控制增强，似乎名称起的太大了），是我临时赶工期开发的一个用于进行世界数据访问和修改的Mod，内容很乱，目前功能较不完善且仅支持1.16.4和1.16.5，但是够这次使用，可以在以下地址下载。

> MOD:
>
> [https://github.com/lovexyn0827/MessMod/releases/tag/1.16.4-20220408](https://github.com/lovexyn0827/MessMod/releases/tag/1.16.4-20220408)
>
> README:
>
> [https://github.com/lovexyn0827/MessMod/blob/main/README.md](https://github.com/lovexyn0827/MessMod/blob/main/README.md)。

实体运动研究中不能过于相信贴图（或者说是客户端上显示出的实体以及碰撞箱），因为贴图位置比在服务端上实体的真正位置通常是滞后的，研究过程中太相信贴图那么可以认为第一步就输了，而这个Mod个人认为最大的功能就是正确地显示服务端上实体的碰撞箱位置，防止被客户端欺骗。

chunkmap是我主要在7月9-18日开发的一个用于可视化区块的加载、生成和区块加载票的Mod，目前功能趋于完善。

> 最新版本下载地址：
>
> [https://github.com/lovexyn0827/Chunkmap/releases/tag/v20210825](https://github.com/lovexyn0827/Chunkmap/releases/tag/v20210825)
>
> MCBBS上的介绍贴：
>
> [https://www.mcbbs.net/thread-1225181-1-1.html](https://www.mcbbs.net/thread-1225181-1-1.html)。

文中涉及所有源代码由minecraft fabric中genSources生成，mapping使用yarn-1.16.4+build.1-v6，如需要可以自行反编译。

该报告的Word/PDF格式（并非最新）以及配套存档下载：

> [https://wwz.lanzoui.com/b02iez40j](https://wwz.lanzoui.com/b02iez40j)  密码5a3e

用到的一些小程序（请在classpath中包含反混淆的Minecraft及其运行库）：

> [https://github.com/lovexyn0827/Entity](https://github.com/lovexyn0827/Entity)。

## 附录D主要符号及单位

这里仿照国际单位制选取时间和长度作为连个基本单位。定义时间是用于描述某一过程经过的运算周期的量，长度是用于描述两个点之间距离的量。常用单位及其换算关系如下，其中格与米是等价的，大家可以按照个人喜好使用，文中以米为准：

表D1主要符号表

| 量       | 单位名     | 符号        | 简要的定义             | 换算           |
|--------|--------|--------|-------|--------|
| 长度     | 米         | m           | 完整方块的棱长         | 1m             |
|            |              |               |                          | =1b            |
|            |              |               |                          | =16px          |
|            |              |               |                          | =1/16区块      |
|            | 格         | b           | 完整方块的棱长         |                  |
|            | 像素       | px          | 方块最小渲染单元的边长 |                  |
|            | 区块       |               | 一个区块俯视图的边长   |                  |
| 时间     | 游戏刻     | gt          | 一个游戏刻代表的时间   | 1gt            |
|            |              |               |                          | =1/20s         |
|            |              |               |                          | =1/2红石刻     |
|            | 无卡顿的秒 | s           | 在TPS为20时的一秒      |                  |
|            | 红石刻     | 无          | 一档红石中继器的延迟   |                  |
| 速度     | 米每刻     | m/gt        |                          | 1m/gt          |
|            |              |               |                          | =20m/s         |
|            | 米每秒     | m/s         |                          |                  |
| 加速度   | 米每平方刻 | $m/gt^2$ |                          | 1$m/gt^2$   |
|            |              |               |                          | =400$m/s^2$ |
|            | 米每平方秒 | $m/s^2$  |                          |                  |
| 阻力系数 | 负一次方刻 | $gt^{-1}$ |                          |                  |

当然，这些单位的使用没有必要那么严格，把仅有m和gt组成的单位都看成1也行。

## 附录E 定义索引

### **A**

AI加速度

### **B**

爆炸半径

爆炸半径利用率

爆炸接触率

爆炸利用率

爆炸伤害半径 

爆炸威力

爆炸影响力

爆炸中心

### **C**

侧向加速度系数

### **D**

地面移动加速度

地面阻力

### **F**

FallDistance

flyingSpeed

forwardSpeed

horizontalCollision

方块网格

方块坐标

飞行时间利用率

飞行移动加速度

俯仰角

### **G**

根实体

固体实体

### **H**

horizontalCollision 

滑度

火球类

### **J**

加速度

加速度利用率

检查方块网格碰撞

接触率利用率

### **K**

可攀登方块

空气阻力

空气阻力系数

### **L**

LivingEntity

流体加速

流体流向向量

流体深度阀值

流体阻力

### **M**

Motion 

movementMultiplier

movementSpeed

### **N**

noClip

### **P**

PersistentProjectileEntity

pistonMovementDelta

pistonMovementTick

碰撞箱

偏航角

### **Q**

前向加速度系数

取样点

### **R**

raycast

### **S**

sidewaysSpeed

stepHeight

实际位移趋势

实体ID

实体基础运算

实体挤压

实体所处方块

实体下方方块

实体着陆方块

输入位移

速度

速度乘数

### **T**

同位实体 

弹射物

投掷物

### **U**

upwardSpeed

### **V**

verticalCollision

### **W**

位移趋势

位移趋势预处理

位移确定

### **X**

向上的加速度系数

### **Y**

沿轴移动

坐标

移动

### **Z**

着地
# 圆锥曲线 常用二级结论附证明过程

## 前言

做这篇文章最初的缘由，似乎也早已忘却了，大抵是期中时拍拍脑子生出的主意，然终竟无法再考究了……然而既已入年，我想自己许是有些寂寞而无所事事了。恰逢 A 君邀我做一篇圆锥曲线的文章，他仿佛有点谑我的意思，欲以此指代方才过去的令人悲哀的数学考题，我举起手机只是说：

“假如一道圆锥曲线填空压轴，它是没有常数且万难算出的，考场上有许多没背二级结论的高中生，见到就跳过了，然而是舍小保大，并不感到挂科的悲哀。现在你教他们背二级结论，说动了想冲高分的几人，使这不幸的少数者来受知晓结论而仍解不出的可能挂科的苦楚，你倒以为对得起他们么？”

“然而几个人既然背了，你不能说决没有解出这个题的希望。”

是的，我虽然自有我的确信，然而说到希望，却是不能抹杀的。因为希望是在于将来，决不能以我之必无的证明，来折服了他之所谓可有，于是我终于答应他也做圆锥曲线的文章了。

{% p right::<i>二零二五年一月十七日，记于成都</i> %}

## 椭圆 基础二级结论

若无特殊说明，椭圆标准方程 $E: \frac{x^2}{a^2}+\frac{y^2}{b^2}=1$ 均满足 $a>b>0$，焦点在 $x$ 轴上。且若无特殊指明，“椭圆 $E$”均指上述的椭圆 $E: \frac{x^2}{a^2}+\frac{y^2}{b^2}=1$。

### 通径

> 在椭圆 $E$ 中，与焦点所在轴垂直的焦点弦被椭圆截得线段的长称作其通径。椭圆的通径长 $d=\frac{2b^2}{a}$。

**评析**：直接将横坐标 $\pm c$ 代入即可解得纵坐标，通径长为纵坐标绝对值的二倍。

**证明**：

横坐标 $c$ 代入椭圆解析式：

$$
\frac{c^2}{a^2}+\frac{y^2}{b^2}=1
$$

得到 $y^2=b^2-b^2e^2$。

因为在椭圆中有 $a^2=b^2+c^2$，因此 $c^2=a^2-b^2$，椭圆离心率还可以表示成 $e=\frac{c}{a}=\sqrt{\frac{c^2}{a^2}}=\sqrt{\frac{a^2-b^2}{a^2}}=\sqrt{1-\frac{b^2}{a^2}}$。代入得：

$$
\begin{aligned}
y^2&=b^2-e^2b^2
\\&=b^2-(1-\frac{b^2}{a^2})b^2
\\&=\frac{b^4}{a^2}
\\y&=\pm\frac{b^2}{a}
\end{aligned}
$$

此时 $d=2|y|=\frac{2b^2}{a}$。

证毕。

### 圆周定理

> 在椭圆 $E$ 中，$A,B$ 是椭圆上关于原点对称的两点，$M$ 是椭圆上异于 $A,B$ 的一点。那么直线 $AM,BM$ 的斜率之积为 $-\frac{b^2}{a^2}$。

**评析**：也不需要什么特殊的技巧，就是设点硬算。这个结论是必背的经典二级结论之一。

**证明**：

设 $A(x_1,y_1)~B(-x_1,-y_1)~M(x_2,y_2)$。那么两直线斜率之积可以表示为 $k_{AM}k_{BM}$，即：

$$
\begin{aligned}
k_{AM}\cdot k_{BM}&=\frac{y_2-y_1}{x_2-x_1}\times\frac{y_2+y_1}{x_2+x_1}
\\&=\frac{y_2^2-y_1^2}{x_2^2-x_1^2}
\end{aligned}
$$

三点都在椭圆上，代入椭圆解析式得关系式：

$$
\begin{cases}
\dfrac{x_1^2}{a^2}+\dfrac{y_1^2}{b^2}=1
\\\qquad
\\\dfrac{x_2^2}{a^2}+\dfrac{y_2^2}{b^2}=1
\end{cases}\rightarrow\begin{cases}
y_1^2=b^2-\dfrac{b^2x_1^2}{a^2}
\\\qquad
\\y_2^2=b^2-\dfrac{b^2x_2^2}{a^2}
\end{cases}
$$

将 $y_1^2$ 和 $y_2^2$ 用 $x_1^2,x_2^2$ 表示出来：

$$
\begin{aligned}
&=\dfrac{\frac{b^2}{a^2}(x_1^2-x_2^2)}{x_2^2-x_1^2}
\\&=-\frac{b^2}{a^2}
\end{aligned}
$$

证毕。

**拓展变形**：我们默认椭圆的焦点位于 $x$ 轴，那万一焦点在 $y$ 轴上呢？首先我们需要保证较大的分母为 $a$，较小的为 $b$，例如 $\frac{y^2}{9}+\frac{x^2}{4}=1$，此时 $a^2=9,b^2=4$，现在的两直线斜率之积为 $-\frac{9}{4}$，即 $-\frac{a^2}{b^2}$，分子分母调换了！做题时一定要注意，证明方法同上。

### 广义垂径定理/中点弦公式

> 在椭圆 $E$ 中，$A,B$ 为椭圆上两点，$M$ 为弦 $AB$ 的中点，那么直线 $OM$ 与直线 $AB$ 的斜率之积为 $-\frac{b^2}{a^2}$。

**评析**：处理中点的方法一共有两个——常规联立法和点差法。此处我们使用第一种，因为韦达定理可以很轻松的表示出中点的坐标；同时设出直线 $AB$ 代表我们可以只用一个 $k$ 表示其斜率，由于 $OM$ 过原点，表示它的斜率也是容易的。那我们就开始吧。

**证明**：

设直线 $AB:y=kx+m$。斜率不存在时无意义，故斜率一定存在。联立方程：

$$
\begin{cases}
y=kx+m
\\\frac{x^2}{a^2}+\frac{y^2}{b^2}=1
\end{cases}
$$

得：

$$
\begin{aligned}
b^2x^2+a^2(k^2x^2+2mkx+m^2)-a^2b^2&=0
\\(b^2+a^2k^2)x^2+2a^2mkx+a^2m^2-a^2b^2&=0
\end{aligned}
$$

根据韦达定理得：

$$
x_1+x_2=-\frac{2a^2mk}{b^2+a^2k^2},x_1x_2=\frac{a^2m^2-a^2b^2}{b^2+a^2k^2}
$$

因此 $M\left(-\dfrac{a^2mk}{b^2+a^2k^2},\dfrac{b^2m}{b^2+a^2k^2}\right)$。得到斜率乘积为 $k\cdot\left(-\dfrac{b^2m}{a^2mk}\right)=-k\cdot\dfrac{b^2}{a^2k}=-\dfrac{b^2}{a^2}$。

证毕。

**拓展变形**：易错点与上一个结论相同，焦点所在坐标轴改变后，乘积会从原先的 $-\frac{b^2}{a^2}$ 变成 $-\frac{a^2}{b^2}$。

### 焦半径公式

> 令 $F_1,F_2$ 为椭圆 $E$ 的左右焦点，$P(x_0,y_0)$ 为椭圆上一点，那么 $|PF_1|=a+ex_0,|PF_2|=a-ex_0$。其中 $e=\frac{c}{a}$，即椭圆的离心率。

**评析**：这个结论其实就是椭圆第二定义的变形式，不信你看。

**证明**：

先证 $|PF_1|=a+ex_0$。对于 $F_1$ 来说，对应的准线为直线 $x=-\frac{a^2}{c}$。根据椭圆第二定义有：

$$
\begin{aligned}
\dfrac{|PF_1|}{x_0+\frac{a^2}{c}}&=e
\\\dfrac{|PF_1|}{x_0+\frac{a}{e}}&=e
\\|PF_1|&=ex_0+a
\end{aligned}
$$

再证 $|PF_2|=a-ex_0$。其实根据椭圆第一定义 $|PF_1|+|PF_2|=2a$ 即可推出它，但是我们继续用第二定义推导。此时对应的准线是直线 $x=\frac{a^2}{c}$：

$$
\begin{aligned}
\dfrac{|PF_2|}{\frac{a}{e}-x_0}&=e
\\|PF_2|&=a-ex_0
\end{aligned}
$$

证毕。

**拓展变形**：焦点在 $y$ 轴上时，结论变为 $|PF_1|=a+ey_0,|PF_2|=a-ey_0$。

### 焦点三角形相关

> 椭圆的左右焦点 $F_1,F_2$ 与椭圆上一点 $P$ 组成的三角形 $\triangle PF_1F_2$ 称作这个椭圆的焦点三角形。

本节中出现的角 $\theta$ 若无特殊说明均指代 $\angle F_1PF_2$。

#### 取值范围

> 焦点三角形 $\triangle PF_1F_2$ 中，$|PF_1|\in(a-c,a+c),|PF_2|\in(a-c,a+c),|PF_1||PF_2|\leq a^2$。

**评析**：前两个非常好证，他们理论上在 $P$ 与左右端点重合时取到最值，但是此时 $P,F_1,F_2$ 三点共线，因此不是三角形，所以是开区间。对于第三个，乘积的取值范围，则需要基本不等式。

**证明**：

根据基本不等式有：

$$
|PF_1||PF_2|\leq\left(\frac{|PF_1|+|PF_2|}{2}\right)^2=a^2
$$

证毕。

#### 周长

> 焦点三角形 $\triangle PF_1F_2$ 的周长 $C_{\triangle PF_1F_2}=|PF_1|+|PF_2|+|F_1F_2|=2a+2c$。

**评析**：根据椭圆的第一定义来的，$|PF_1|+|PF_2|=2a,|F_1F_2|=2c$。

#### 面积

> 焦点三角形 $\triangle PF_1F_2$ 的面积 $S_{\triangle F_1F_2}=b^2\tan\frac{\theta}{2}$。

**评析**：出现角度和面积，我们需要想到正/余弦定理。根据正弦定理的三角形面积公式 $S=\frac{1}{2}ab\sin\theta$ 以及余弦定理的 $c^2=a^2+b^2-2ab\cos\theta$，我们可以解决大部分与边长和角度有关的圆锥曲线证明/求值问题。

**证明**：

由正弦定理得，$S_{\triangle PF_1F_2}=\frac{1}{2}|PF_1||PF_2|\sin\theta$。

在 $\triangle PF_1F_2$ 中运用余弦定理：$|F_1F_2|^2=4c^2=|PF_1|^2+|PF_2|^2-2|PF_1||PF_2|\cos\theta$，得到 $|PF_1||PF_2|=\dfrac{|PF_1|^2+|PF_2|^2-4c^2}{2\cos\theta}$。

同时根据完全平方公式，$|PF_1|^2+|PF_2|^2=(|PF_1|+|PF_2|)^2-2|PF_1||PF_2|=4a^2-2|PF_1||PF_2|$，代入上式移项解得 $|PF_1||PF_2|=\dfrac{2(a^2-c^2)}{1+\cos\theta}$，根据面积公式可得 $S=\dfrac{(a^2-c^2)\sin\theta}{1+\cos\theta}=\dfrac{b^2\sin\theta}{1+\cos\theta}=b^2\tan\dfrac{\theta}{2}$。

证毕。

**拓展变形**：三角函数的半角公式（附证明）。

——正/余弦半角公式

根据余弦倍角公式的变形式 $\cos2\theta=2\cos^2\theta-1$，将 ${2}\theta$ 换成 $\theta$，$\theta$ 换成 $\frac{\theta}{2}$ 即得 $\cos\theta=2\cos^2\frac{\theta}{2}-1$，$\cos\frac{\theta}{2}=\sqrt{\frac{\cos\theta+1}{2}}$。

同理，对于正弦函数，有 $\cos2\theta=1-2\sin^2\theta\rightarrow\cos\theta=1-2\sin^2\frac{\theta}{2}\rightarrow\sin\frac{\theta}{2}=\sqrt{\frac{1-\cos\theta}{2}}$。

——正切半角公式

由正切函数定义可得 $\tan\frac{\theta}{2}=\dfrac{\sin\frac{\theta}{2}}{\cos\frac{\theta}{2}}$，利用三角函数的升幂，也就是上面导出正余弦半角公式时使用的余弦倍角公式，分子分母同乘 $\cos\frac{\theta}{2}$ 可得：$\tan\frac{\theta}{2}=\dfrac{\sin\frac{\theta}{2}\cos\frac{\theta}{2}}{\cos^2\frac{\theta}{2}}=\dfrac{\frac{1}{2}\sin\theta}{\frac{1}{2}(1+\cos\theta)}=\dfrac{\sin\theta}{\cos\theta+1}$。

因此证明面积公式时出现的 $\frac{\sin\theta}{\cos\theta+1}$ 可以换成 $\tan\frac{\theta}{2}$。三个公式汇总起来就是：

$$
\sin\frac{\theta}{2}=\sqrt{\frac{1-\cos\theta}{2}}\qquad\cos\frac{\theta}{2}=\sqrt{\frac{\cos\theta+1}{2}}\qquad\tan\frac{\theta}{2}=\frac{\sin\theta}{\cos\theta+1}
$$

#### 内切圆

> 焦点三角形 $\triangle PF_1F_2$ 的内切圆半径为 $\frac{c}{\sin\theta}$，已知半径也可求出顶角 $\sin\theta=\frac{c}{R}$。

**评析**：这一条其实也没什么，主要是正弦定理的运用。因为在三角形中 $\frac{a}{\sin A}=\frac{b}{\sin B}=\frac{c}{\sin C}=2R$，其中 $R$ 就是内切圆半径。将 $\theta$ 所对的边 $F_1F_2$ 的长度代入即可证得该结论。

#### 离心率公式

> 令焦点三角形 $\triangle PF_1F_2$ 的底角 $\angle PF_1F_2=\alpha,\angle PF_2F_1=\beta$，那么椭圆的离心率 $e=\frac{\sin(\alpha+\beta)}{sin\alpha+\sin\beta}=\frac{\sin\theta}{\sin\alpha+\sin\beta}$。

**评析**：有角有边，当然考虑正余弦定理。

**证明**：

易知此时 $\theta=\pi-\alpha-\beta$。根据正弦定理有 $\frac{2c}{\sin(\pi-\alpha-\beta)}=\frac{2c}{\sin(\alpha+\beta)}=\frac{|PF_1|}{\sin\beta}=\frac{|PF_2|}{\sin\alpha}$。在椭圆中又有 $|PF_1|+|PF_2|=2a$，那么 $|PF_2|=2a-|PF_1|$。

代入连等式中，得到 $\frac{2c}{\sin(\alpha+\beta)}=\frac{|PF_1|}{\sin\beta}=\frac{2a-|PF_1|}{\sin\alpha}$，根据后两项可以解出 $|PF_1|=\frac{2a\sin\beta}{\sin\alpha+\sin\beta}$，此时代入第二项得到 $\frac{2c}{\sin(\alpha+\beta)}=\frac{2a}{\sin\alpha+\sin\beta}$。

此时 $\frac{c}{a}=e=\frac{\sin(\alpha+\beta)}{\sin\alpha+\sin\beta}=\frac{\sin\theta}{\sin\alpha+\sin\beta}$。

证毕。

## 双曲线 基础二级结论

若无特殊说明，双曲线标准方程 $E: \frac{x^2}{a^2}-\frac{y^2}{b^2}=1$，满足 $a>0,b>0,a\neq b$，焦点在 $x$ 轴上。且若无特殊说明，“双曲线 $E$”均指上述的标准双曲线 $E:\frac{x^2}{a^2}-\frac{y^2}{b^2}=1$。

### 通径

> 在双曲线 $E$ 中，与焦点所在轴垂直的焦点弦被双曲线截得线段的长称作其通径。双曲线的通径长 $d=\frac{2b^2}{a}$。

**评析**：与椭圆证法相同。

**证明**：

将横坐标 $\pm c$ 代入得 $y^2=b^2e^2-b^2$。因为双曲线满足 $c^2=a^2+b^2$，可以推导出 $e=\sqrt{1+\frac{b^2}{a^2}}$。那么 $y^2=\frac{b^4}{a^2}$，得到 $y=\pm\frac{2b^2}{a}$。此时通径长为 $d=2|y|=\frac{2b^2}{a}$。

证毕。

### 圆周定理

> 在双曲线 $E$ 中，$A,B$ 是双曲线上关于原点对称的两点，$M$ 是双曲线上异于 $A,B$ 的一点。那么直线 $AM,BM$ 的斜率之积为 $\frac{b^2}{a^2}$。

**评析**：双曲线有关二级结论的证明思路和椭圆基本相同，这里我们沿用椭圆的证明方法继续硬算。

**证明**：

设 $A(x_1,y_1)~B(-x_1,-y_1)~M(x_2,y_2)$，那么：

$$
\begin{aligned}
k_{AM}\cdot k_{BM}&=\frac{y_2-y_1}{x_2-x_1}\times\frac{y_2+y_1}{x_2+x_1}
\\&=\frac{y_2^2-y_1^2}{x_2^2-x_1^2}
\end{aligned}
$$

三点都在双曲线上，得到：

$$
\begin{cases}
y_1^2=\dfrac{b^2x_1^2}{a^2}-b^2
\\\qquad
\\y_2^2=\dfrac{b^2x_2^2}{a^2}-b^2
\end{cases}
$$

代入得：

$$
\begin{aligned}
&=\dfrac{\frac{b^2}{a^2}(x_2^2-x_1^2)}{x_2^2-x_1^2}
\\&=\frac{b^2}{a^2}
\end{aligned}
$$

证毕。

**拓展变形**：焦点所在坐标轴改变时同样要变成 $\frac{a^2}{b^2}$。

### 广义垂径定理/中点弦公式

> 在双曲线 $E$ 中，$A,B$ 为双曲线上两点，$M$ 为弦 $AB$ 的中点，那么直线 $OM$ 与直线 $AB$ 的斜率之积为 $\frac{b^2}{a^2}$。

**评析**：同样使用椭圆的证明方法

**证明**：

令直线 $AB: y=kx+m$，斜率不存在时无意义，故斜率存在。联立直线和双曲线方程：

$$
\begin{cases}
y=kx+m
\\\frac{x^2}{a^2}-\frac{y^2}{b^2}=1
\end{cases}
$$

得到：$(b^2-a^2k^2)x^2-2a^2mkx-a^2m^2-a^2b^2=0$。韦达定理得 $x_1+x_2=\dfrac{2a^2mk}{b^2-a^2k^2},x_1x_2=-\dfrac{a^2m^2+a^2b^2}{b^2-a^2k^2}$。

得到中点坐标 $M\left(\dfrac{a^2mk}{b^2-a^2k^2},\dfrac{b^2m}{b^2-a^2k^2}\right)$，此时斜率之积表示为：

$$
\begin{aligned}
k_{AB}\cdot k_{OM}&=k\cdot\dfrac{b^2m}{a^2mk}
\\&=k\cdot\dfrac{b^2}{a^2k}
\\&=\frac{b^2}{a^2}
\end{aligned}
$$

证毕。

**拓展变形**：焦点在 $y$ 轴上时对应的乘积是 $\frac{a^2}{b^2}$。

### 焦半径公式

> 令 $F_1,F_2$ 为双曲线 $E$ 的左右焦点，$P(x_0,y_0)$ 为双曲线上一点，$P$ 在右支上时有 $|PF_1|=a+ex_0,|PF_2|=-a+ex_0$；在左支上时有 $|PF_1|=-a-ex_0,|PF_2|=a-ex_0$。

**评析**：双曲线第二定义的变形

**证明**：

当 $P$ 在右支时，根据第二定义，有 $\dfrac{|PF_1|}{\frac{a^2}{c}+x_0}=\dfrac{|PF_1|}{\frac{a}{e}+x_0}=e$，得到 $|PF_1|=a+ex_0$，然后根据双曲线中 $||PF_1|-|PF_2||=2a$ 可得 $|PF_2|=-a+ex_0$。

同理可以证得左支公式。

证毕。

**拓展变形**：焦点在 $y$ 轴上时要把 $x_0$ 换成 $y_0$。

### 渐近线相关

> 过原点且在无穷远处与双曲线的距离无限趋近于 ${0}$ 的两条直线叫做这个双曲线的渐近线。焦点在 $x$ 轴上时渐近线的解析式为 $y=\pm\frac{b}{a}x$；若在 $y$ 轴上则为 $y=\pm\frac{a}{b}x$，即 $x=\pm\frac{b}{a}y$。

#### 焦点-渐近线距离

> 双曲线的焦点与任意一条渐近线的距离均为 $b$。

**评析**：使用点到直线的距离公式证明。

**证明**：

左焦点 $F_1(-c,0)$，到渐近线 $y\pm\frac{b}{a}x=0$ 的距离为：

$$
d=\dfrac{\frac{b}{a}c}{\sqrt{1+\frac{b^2}{a^2}}}=\dfrac{eb}{e}=b
$$

证毕。

### 焦点三角形相关

> 双曲线的左右焦点 $F_1,F_2$ 与双曲线上一点 $P$ 组成的三角形 $\triangle PF_1F_2$ 称作这个双曲线的焦点三角形。

本节中出现的角 $\theta$ 若无特殊说明均指代 $\angle F_1PF_2$。

#### 周长

> 焦点三角形 $\triangle PF_1F_2$ 的周长为 ${2}e|x_0|+2c$。

**评析**：根据前面所证明的焦半径公式可得这个结论。

#### 面积

> 焦点三角形 $\triangle PF_1F_2$ 的面积为 $\dfrac{b^2}{\tan\frac{\theta}{2}}=b^2\cot\frac{\theta}{2}$。

**证明**：

正弦定理得：$S=\frac{1}{2}|PF_1||PF_2|\sin\theta$。余弦定理得：${4}c^2=|PF_1|^2+|PF_2|^2-2|PF_1||PF_2|\cos\theta$，得到 $|PF_1||PF_2|=\dfrac{|PF_1|^2+|PF_2|^2-4c^2}{2\cos\theta}$。根据完全平方公式，有 $(|PF_1|-|PF_2|)^2=4a^2=|PF_1|^2+|PF_2|^2-2|PF_1||PF_2|$，联立可得 $|PF_1||PF_2|=\dfrac{|PF_1||PF_2|+2a^2-2c^2}{\cos\theta}$，解得 $|PF_1||PF_2|=\dfrac{2b^2}{1-\cos\theta}$。代入面积公式得 $S=\dfrac{b^2\sin\theta}{1-\cos\theta}=b^2\cot\frac{\theta}{2}$。

证毕。

**拓展变形**：余切的半角公式证明。

$$
\begin{aligned}
\cot\frac{\theta}{2}&=\dfrac{\cos\frac{\theta}{2}}{\sin\frac{\theta}{2}}
\\&=\dfrac{\sin\frac{\theta}{2}\cos\frac{\theta}{2}}{\sin^2\frac{\theta}{2}}
\\&=\dfrac{\frac{1}{2}\sin\theta}{\frac{1}{2}(1-\cos\theta)}
\\&=\dfrac{\sin\theta}{1-\cos\theta}
\end{aligned}
$$

#### 离心率公式

> 令焦点三角形 $\triangle PF_1F_2$ 的底角 $\angle PF_1F_2=\alpha,\angle PF_2F_1=\beta$，那么双曲线的离心率为 $e=\dfrac{\sin\theta}{\sin\beta-\sin\alpha}$。

**证明**：

由正弦定理，$\frac{2c}{\sin\theta}=\frac{|PF_1|}{\sin\beta}=\frac{|PF_2|}{\sin\alpha}$，不妨假设当前 $P$ 在右支上，那么 $|PF_1|-|PF_2|=2a$，即 $|PF_2|=|PF_1|-2a$。解得 $|PF_1|=\frac{2a\sin\beta}{\sin\beta-\sin\alpha}$。此时有 $\frac{2c}{\sin\theta}=\frac{2a}{\sin\beta-\sin\alpha}$。得到 $e=\frac{c}{a}=\frac{\sin\theta}{\sin\beta-\sin\alpha}$。

证毕。

## 抛物线基础二级结论

若无特殊说明，抛物线标准方程 $E: y^2=2px$ 均满足 $p>0$，焦点在 $x$ 轴正半轴。且若无特殊指明，“抛物线 $E$”均指上述的抛物线 $E:y^2=2px$。

### 通径

> 抛物线的通径长为 $2p$。

**评析**：抛物线中只要涉及到焦半径相关的内容，都要第一时间想到焦半径长等于该点与准线的距离从而进行转化，这样可以简化计算。

**证明**：

横坐标 $\frac{p}{2}$ 代入，得到焦半径为 $\frac{p}{2}+\frac{p}{2}=p$，通径为二倍焦半径，即 $2p$。

证毕。

### 焦点弦定理

> 抛物线 $E$ 的一条焦点弦交抛物线于 $A,B$ 两点，那么直线 $OA$ 与直线 $OB$ 的乘积为定值 $-4$。

**评析**：我们可以恰当选择直线的横截式和斜截式来方便计算。在本例中，由于抛物线方程的二次项在 $y$ 上，并且直线过 $x$ 轴上的定点，我们自然地选择横截式来进行计算。

**证明**：

令直线 $AB: x=ty+\frac{p}{2}$，联立抛物线方程 $y^2=2px$ 得：

$$
\begin{aligned}
y^2&=2pty+p^2
\\y^2-2pty-p^2&=0
\end{aligned}
$$

根据韦达定理，得：

$$
y_1+y_2=2pt\qquad y_1y_2=-p^2
\\x_1+x_2=2t(y_1+y_2)+p=4t^2p+p\qquad x_1x_2=t^2y_1y_2+\frac{pt}{2}(y_1+y_2)+\frac{p^2}{4}=\frac{p^2}{4}
$$

斜率的乘积表示为：

$$
\begin{aligned}
k_{OA}\cdot k_{OB}&=\frac{y_1y_2}{x_1x_2}
\\&=-\dfrac{p^2}{\frac{p^2}{4}}
\\&=-4
\end{aligned}
$$

证毕。

**拓展变形**：事实上，证明过程中由韦达定理导出的关系式 $x_1x_2=\frac{p^2}{4}$ 和 $y_1y_2=-p^2$ 在实践中更为常用一些。

### 两点弦公式

> 抛物线 $E$ 上两点 $A(x_1,y_1)$ 和 $B(x_2,y_2)$ 组成的弦 $AB$ 的斜率为 $\frac{2p}{y_1+y_2}$。

**评析**：适时避开繁琐的高次计算是非常有用的。

**证明**：

因为两点在抛物线上，因此坐标满足：

$$
\begin{cases}
y_1^2=2px_1
\\y_2^2=2px_2
\end{cases}\rightarrow\begin{cases}
x_1=\dfrac{y_1^2}{2p}
\\\qquad
\\x_2=\dfrac{y_2^2}{2p}
\end{cases}
$$

所以斜率可以表示为：$\dfrac{y_2-y_1}{x_2-x_1}=\dfrac{y_2-y_1}{\frac{y_2^2-y_1^2}{2p}}=\dfrac{2p(y_2-y_1)}{(y_1+y_2)(y_2-y_1)}=\dfrac{2p}{y_1+y_2}$。

证毕。

### 焦半径公式

> 抛物线 $E$ 的焦点弦 $AB$ 分别在第一象限和第四象限交抛物线于 $A,B$ 两点，直线 $AB$ 与 $x$ 轴的夹角是 $\theta$，那么 $|AF|=\dfrac{p}{1-\cos\theta},|BF|=\dfrac{p}{1+\cos\theta},|AB|=\dfrac{2p}{\sin^2\theta}$。

**评析**：直接看不太容易，来一张图辅助一下：

![](https://cdn.luogu.com.cn/upload/image_hosting/u81ij962.png)

**证明**：

由抛物线定义知：$|AH|=|AF|=|GH|+|AG|=|GH|+|AF|\cos\theta=p+|AF|\cos\theta$，移项可得 $|AF|=\dfrac{p}{1-\cos\theta}$。同理可证得 $|BF|=\frac{p}{1+\cos\theta}$。

此时 $|AB|=|AF|+|BF|=\dfrac{p}{1-\cos\theta}+\dfrac{p}{1+\cos\theta}=\dfrac{2p}{\sin^2\theta}$。

证毕。

## 椭圆-双曲线共焦点问题

在本章中，我们默认存在一个椭圆 $E_1: \frac{x^2}{a_1^2}+\frac{y^2}{b_1^2}=1$ 与 $E_2:\frac{x^2}{a_2^2}-\frac{y^2}{b_2^2}=1$ 共焦点。若无特殊说明，$P$ 为两圆锥曲线在第一象限内的交点，$\angle F_1PF_2=\theta$。如下图：

![](https://cdn.luogu.com.cn/upload/image_hosting/njrbhs9j.png)

### 焦半径

> 共焦点的椭圆和双曲线满足 $|PF_1|=a_1+a_2,|PF_2|=a_1-a_2$。

**评析**：注意利用好椭圆和双曲线的定义。

**证明**：

在椭圆中，有 $|PF_1|+|PF_2|=2a_1$；在双曲线中，有 $|PF_1|-|PF_2|=2a_2$，两式相加得 ${2}|PF_1|=2a_1+2a_2$，相减得 ${2}|PF_2|=2a_1-2a_2$。由此得到：

$$
|PF_1|=a_1+a_2\qquad |PF_2|=a_1-a_2
$$

证毕。

### 离心率与角的关系

> 共焦点的椭圆和双曲线满足 $\dfrac{\sin^2\frac{\theta}{2}}{e_1^2}+\dfrac{\cos^2\frac{\theta}{2}}{e_2^2}=1$

**评析**：同样是有角有边，考虑正/余弦定理。这个结论可以帮助你快速解决诸如 $e_1^2e_2^2,\frac{1}{e_1^2}+\frac{1}{e_2^2}$ 等式子的最值问题。

**证明**：

借用上一节的焦半径结论，并综合余弦定理，可以得到：

$$
\begin{aligned}
a_1^2+a_2^2+2a_1a_2+a_1^2+a_2^2-2a_1a_2-2(a_1^2-a_2^2)\cos\theta&=4c^2
\\2a_1^2+2a_2^2-2a_1^2\cos\theta+2a_2^2\cos\theta&=4c^2
\\(1-\cos\theta)a_1^2+(1+\cos\theta)a_2^2&=2c^2
\\\dfrac{(1-\cos\theta)a_1^2}{2c^2}+\dfrac{(1+\cos\theta)a_2^2}{2c^2}&=1
\\\dfrac{1-\cos\theta}{2e_1^2}+\dfrac{1+\cos\theta}{2e_2^2}&=1
\\\dfrac{\sin^2\frac{\theta}{2}}{e_1^2}+\dfrac{\cos^2\frac{\theta}{2}}{e_2^2}&=1
\end{aligned}
$$

证毕。

**拓展变形**：正余弦函数的升幂/降幂公式。

由余弦的二倍角公式 $\cos\theta=2\cos^2\frac{\theta}{2}-1=1-2\sin^2\frac{\theta}{2}$，得到 $\sin^2\frac{\theta}{2}=\frac{1-\cos\theta}{2},\cos^2\frac{\theta}{2}=\frac{1+\cos\theta}{2}$。即证得降幂公式。事实上，余弦的二倍角公式就是升幂公式。

## 蒙日圆

椭圆 $E$ 上任意两条互相垂直的切线焦点的轨迹组成了一个圆，称作蒙日圆/外准圆。椭圆 $\frac{x^2}{a^2}+\frac{y^2}{b^2}=1$ 的蒙日圆为 $x^2+y^2=a^2+b^2$。如下图：

![](https://cdn.luogu.com.cn/upload/image_hosting/dmkg7pq2.png)

若无特殊说明，两切线交于 $P$，且与椭圆分别交于点 $A$ 和 $B$，与蒙日圆分别交于点 $C$ 和 $D$。

### 轨迹方程

> 椭圆 $E$ 对应的蒙日圆方程为 $x^2+y^2=a^2+b^2$。

**评析**：没有感情，只有设点。

**证明**：

切线斜率不存在时，$P(\pm a,\pm b)$，显然在圆 $x^2+y^2=a^2+b^2$ 上。

切线斜率存在时，设 $PM:y=kx+m$，则根据垂直关系有 $PN:y=-\frac{1}{k}x+n$。

联立 $PM$ 与椭圆方程，并根据相切关系得：

$$
\begin{aligned}
(b^2+a^2k^2)x^2+2a^2mkx+a^2m^2-a^2b^2&=0
\\\Delta&=0
\\4a^4m^2k^2-4a^2(b^2+a^2k^2)(m^2-b^2)&=0
\\a^2k^2+b^2-m^2&=0
\\m^2&=a^2k^2+b^2
\end{aligned}
$$

同理可得 $\frac{a^2}{k^2}+b^2-n^2=0\rightarrow a^2+b^2k^2=n^2k^2$。

联立两直线方程得到 $P\left(\frac{k(n-m)}{k^2+1},\frac{nk^2+m}{k^2+1}\right)$，此时 $|OP|^2=\frac{n^2k^2+m^2}{k^2+1}=\frac{a^2+b^2k^2+a^2k^2+b^2}{k^2+1}=a^2+b^2$。因此 $P$ 在圆 $x^2+y^2=a^2+b^2$ 上。

证毕。

### 几何性质 其一

> 蒙日圆上一点 $P$ 引出的两条切线交蒙日圆于 $C,D$ 两点，直线 $CD$ 过原点。

**评析**：无

**证明**：

根据圆内直径所对的圆周角恒为直角的关系，可得 $CD$ 为蒙日圆直径，即 $C,O,D$ 三点共线、$CD$ 过原点。

证毕。

### 广义垂径定理

> $P$ 为蒙日圆上一点，过 $P$ 作椭圆 $E$ 的两条切线 $PA,PB$，切点为 $A,B$，连接 $OP$，则 $k_{OP}\cdot k_{AB}=-\frac{b^2}{a^2}$。

**评析**：利用圆锥曲线的切点弦方程即可快速解决。

**证明**：

令 $P(x_0,y_0)$，那么 $k_{OP}=\frac{y_0}{x_0}$。根据圆锥曲线的切点弦公式，得到切点弦 $AB:\frac{x_0}{a^2}x+\frac{y_0}{b^2}y=1$，得到 $k_{AB}=-\frac{b^2x_0}{a^2y_0}$。相乘即得结果 $-\frac{b^2}{a^2}$。

证毕。

**拓展变形**：椭圆交点所在坐标轴变化后仍然会变成 $-\frac{a^2}{b^2}$。同时根据结果和中点弦公式可以得知 $AB$ 与 $OP$ 的交点 $M$ 为 $AB$ 中点。

### 几何性质 其二

> 蒙日圆上一点 $P$ 向椭圆引两条切线 $PA$ 和 $PB$，交椭圆于 $A,B$，交蒙日圆于 $C,D$，$OP$ 交 $AB$ 于 $M$ 点，有 $AB//CD$。

**评析**：利用几何关系进行证明。前置是上面的广义垂径定理和几何性质一。

**证明**：

根据蒙日圆，得到顶角 $\angle APB=90\degree$。根据上面广义垂径定理得到的 $M$ 为 $AB$ 中点的关系，结合直角三角形斜边上的中线定理，可以得到 $PM=PA=PB$，所以 $\angle APO=\angle OAP$。同样在大直角三角形 $PCD$ 中类似地又有 $\angle DCP=\angle OAP$，因此 $\angle DCP=\angle APO$。同位角相等，两直线平行。

证毕。

**拓展变形**：根据这条性质，广义垂径定理可以推广成 $k_{OP}\cdot k_{CD}=-\frac{b^2}{a^2}$。

### 几何性质 其三

> 从蒙日圆上一点 $P$ 向椭圆 $E$ 引两条切线 $PA,PB$，切点为 $A,B$。那么 $k_{OA}k_{AP}=k_{OB}k_{BP}=-\frac{b^2}{a^2},k_{OA}k_{OB}=-\frac{b^4}{a^4}$。

**评析**：运用切线公式和已知的垂直条件快速解题。

**证明**：

令 $A(x_1,y_1),B(x_2,y_2)$，则根据切线公式得 $PA:\frac{x_1}{a^2}x+\frac{y_1}{b^2}y=1$，斜率为 $-\frac{b^2x_1}{a^2y_1}$，乘积为 $-\frac{b^2x_1}{a^2y_1}\cdot\frac{y_1}{x_1}=-\frac{b^2}{a^2}$。同理可以证得 $k_{OB}k_{PB}=-\frac{b^2}{a^2}$。

综合以上两式 $k_{OA}k_{PA}=k_{OB}k_{PB}=-\frac{b^2}{a^2}$，得 $k_{OA}k_{OB}k_{PA}k_{PB}=\frac{b^4}{a^4}$，根据蒙日圆的切线垂直条件 $k_{PA}k_{PB}=-1$，得到 $k_{OA}k_{OB}=-\frac{b^4}{a^4}$。

证毕。

## 阿基米德三角形

抛物线的某条弦 $AB$，过 $A,B$ 的两条抛物线的切线相交于 $P$ 点，三角形 $PAB$ 称作这个抛物线的阿基米德三角形。如下图：

![](https://cdn.luogu.com.cn/upload/image_hosting/g9xstusr.png)

$\triangle ABP$ 和 $\triangle CDQ$ 都是这个抛物线的阿基米德三角形。

若无特殊说明，本章中的抛物线 $E$ 均指代抛物线 $y^2=2px(p>0)$。

### 几何性质 其一

> 阿基米德三角形在抛物线上的弦的中点为 $M$，那么该弦所对的顶点 $P$ 满足 $PM//x$。

**评析**：巧妙运用切线方程解决问题。

**证明**：

令弦的端点 $A(x_1,y_1),B(x_2,y_2)$，点在抛物线上得 $x_1=\frac{y_1^2}{2p},x_2=\frac{y_2^2}{2p}$。根据切线方程得 $PA:y_1y=px+px_1$，同理得 $PB:y_2y=px+px_2$，联立解得交点 $P(\frac{y_1y_2}{2p},\frac{y_1+y_2}{2})$。中点得 $M(\frac{y_1^2+y_2^2}{4p},\frac{y_1+y_2}{2})$，得到 $PM//x$。

证毕。

### 几何性质 其二

> 当阿基米德三角形在抛物线上的弦过顶点 $G(x_0,y_0)$ 时，该弦所对顶点的运动轨迹为 $y_0y=p(x+x_0)$。

**评析**：利用切点弦公式，或者是几何性质一可以证明。此处选用几何性质一进行证明。

**证明**：

令底边 $A(x_1,y_1),B(x_2,y_2)$，根据几何性质一得顶点 $P(\frac{y_1y_2}{2},\frac{y_1+y_2}{2})$。因为定点 $G$ 在 $AB$ 上，应有 $k_{AB}=k_{AG}$，即：

$$
\begin{aligned}
\dfrac{y_2-y_1}{x_2-x_1}&=\dfrac{y_1-y_0}{x_1-x_0}
\\\dfrac{y_2-y_1}{\frac{y_2^2}{2p}-\frac{y_1^2}{2p}}=\dfrac{2p}{y_1+y_2}&=\dfrac{y_1-y_0}{\frac{y_1^2}{2p}-x_0}
\\y_1^2-2px_0&=y_1^2+y_1y_2-y_0(y_1+y_2)
\\2px_0&=y_0(y_1+y_2)-y_1y_2
\\2px_0&=2y_0y_p-2x_p
\\y_0y_p&=p(x_0+x_p)
\end{aligned}
$$

因此 $P$ 在直线 $y_0y=p(x+x_0)$ 上。

证毕。

**拓展变形**：此结论的推论有——当底边过焦点时，顶点的轨迹为抛物线准线；底边过 $x$ 轴定点 $(a,0)$ 时，顶点轨迹为直线 $x=-a$。

### 几何性质 其三

> 当阿基米德三角形的底边过焦点时，阿基米德三角形的顶角为 ${90}\degree$，即 $PA\perp PB$。

![](https://cdn.luogu.com.cn/upload/image_hosting/h79jgkd2.png)

**评析**：可以借助几何性质一来快速解决。

**证明**：

令 $A(x_1,y_1),B(x_2,y_2)$，由几何性质一可得 $P(\frac{y_1y_2}{2p},\frac{y_1+y_2}{2})$。两切线斜率之积为：

$$
\begin{aligned}
k_1k_2&=\dfrac{y_1-\frac{y_1+y_2}{2}}{x_1-\frac{y_1y_2}{2p}}\times\dfrac{y_2-\frac{y_1+y_2}{2}}{x_2-\frac{y_1y_2}{2p}}
\\&=\dfrac{\frac{y_1-y_2}{2}}{\frac{y_1^2-y_1y_2}{2p}}\times\dfrac{\frac{y_2-y_1}{2}}{\frac{y_2^2-y_1y_2}{2p}}
\\&=\dfrac{p(y_1-y_2)}{y_1(y_1-y_2)}\times\dfrac{p(y_2-y_1)}{y_2(y_2-y_1)}
\\&=\dfrac{p^2}{y_1y_2}
\end{aligned}
$$

最后联系到抛物线焦点弦定理中 $y_1y_2=-p^2$（设直线代入韦达定理得出）可以得到斜率之积为 $-1$，即两直线垂直。

证毕。

### 几何性质 其四

> 在阿基米德三角形中，恒有 $\angle PFA=\angle PFB$。

![](https://cdn.luogu.com.cn/upload/image_hosting/hr0wz0fh.png)

**评析**：几何法搭配解析几何解题较为快速。

**证明**：

过 $A,B$ 分别作准线的垂线 $AA_1,BB_1$，垂足为 $A_1,B_1$，连接 $A_1P,B_1P,A_1F$，$A_1F\cap AP=O$，如下图：

![](https://cdn.luogu.com.cn/upload/image_hosting/5x4tdox5.png)

令 $A(x_1,y_1),B(x_2,y_2)$，根据切线公式可得 $PA:y=\frac{p}{y_1}x+\frac{px_1}{y_1}$，得到斜率 $k_{PA}=\frac{p}{y_1}$。由垂直得 $A_1(-\frac{p}{2},y_1)$，因此 $A_1F$ 斜率为 $-\frac{y_1}{p}$，乘积为 $-1$，有 $AP\perp A_1F$。

在抛物线中，有 $|AA_1|=|AF|$，根据直角三角形 HL 型全等得 $\triangle A_1AO\cong\triangle FAO$，进而有 $\angle A_1AO=\angle FAO$，再次可 SAS 证得 $\triangle A_1AP\cong\triangle FAP$。仿照上述全等推导可证得 $\triangle BFP\cong\triangle BB_1P$。那么 $\angle PFB=\angle BB_1P,\angle PFA=\angle PA_1A$。

根据几何性质一可得，$y_P=\frac{y_1+y_2}{2}$，就有 $A_1P=B_1P$，$\angle PA_1B_1=\angle PB_1A_1$，因此 $\angle PA_1A=\angle PB_1B=90\degree+\angle PA_1B_1$，进而得到 $\angle PFB=\angle PFA$。

证毕。

### 几何性质 其五

> 在阿基米德三角形中，有 $|AF|\cdot|BF|=|PF|^2$。

**评析**：根据性质一得出的点的坐标代入计算即可验证。

**证明**：

根据性质一可得 $P(\frac{y_1y_2}{2p},\frac{y_1+y_2}{2})$，距离公式可得 $|PF|^2=(\frac{y_1y_2}{2p}-\frac{p}{2})^2+(\frac{y_1+y_2}{2})^2=\frac{p^2}{4}+\frac{y_1^2y_2^2}{4p^2}+\frac{y_1^2+y_2^2}{4}$。

同时，在抛物线中满足 $|AF|=x_A+\frac{p}{2}=\frac{y_1^2}{2p}+\frac{p}{2}$；同理有 $|BF|=x_B+\frac{p}{2}=\frac{y_2^2}{2p}+\frac{p}{2}$。相乘：

$$
\begin{aligned}
|AF|\cdot|BF|&=\left(\frac{y_1^2}{2p}+\frac{p}{2}\right)\times\left(\frac{y_2^2}{2p}+\frac{p}{2}\right)
\\&=\frac{y_1^2y_2^2}{4p^2}+\frac{p^2}{4}+\frac{y_1^2+y_2^2}{4}
\\&=|QF|^2
\end{aligned}
$$

证毕。

### 几何性质 其六

> 底边 $AB$ 长为 $a$ 的阿基米德三角形的面积最大值为 $\frac{a^3}{8p}$。

**评析**：利用三角形面积等于底乘高除以二，再对高的长度进行放缩即可。

**证明**：

如图：$PH$ 为 $\triangle APB$ 在 $AB$ 边上的高，$M$ 为 $AB$ 中点。令 $AB:x=ky+b$。

![](https://cdn.luogu.com.cn/upload/image_hosting/qoewo2gf.png)

易知 $|PH|\leq|PM|$，在 $AB\perp x$ 时等号成立。$|AB|=a=\sqrt{(k^2+1)(y_1-y_2)^2}\geq\sqrt{(y_1-y_2)^2}$。

根据性质一，$P(\frac{y_1y_2}{2p},\frac{y_1+y_2}{2})$，$M(\frac{x_1+x_2}{2},\frac{y_1+y_2}{2})$，$|PM|=\frac{x_1+x_2}{2}-\frac{y_1y_2}{2p}=\frac{y_1^2+y_2^2}{4p}-\frac{y_1y_2}{2p}=\frac{(y_1-y_2)^2}{4p}$。

此时 $S_{\triangle APB}\leq\frac{1}{2}a\frac{(y_1-y_2)^2}{4p}\leq\frac{a^3}{8p}$，当且仅当 $AB\perp x$ 时取得等号。

证毕。

## 新定义曲线

### 伯努利双纽线

> 平面内一点 $P$ 到 $x$ 轴两定点 $(\pm a,0)$ 的距离之积为定值 $a^2$ 的曲线叫做伯努利双纽线（简称双纽线），其解析式为 $(x^2+y^2)^2=2a^2(x^2-y^2)$。若定点在 $y$ 轴上则为 $(x^2+y^2)^2=2a^2(y^2-x^2)$。

伯努利双纽线 $(x^2+y^2)^2=18(x^2-y^2)$ 的图像如下：

![](https://cdn.luogu.com.cn/upload/image_hosting/c85ly4hp.png)

#### 轨迹方程

**评析**：设点计算。

**解**：

令 $P(x,y),F_1(-a,0),F_2(a,0)$，$|PF_1||PF_2|=a^2$，可得：

$$
\begin{aligned}
|PF_1||PF_2|&=a^2
\\\sqrt{(x+a)^2+y^2}\sqrt{(x-a)^2+y^2}&=a^2
\\\sqrt{x^2+y^2+a^2-2ax}\sqrt{x^2+y^2+a^2+2ax}&=a^2
\\\sqrt{x^4+y^4+a^4+2x^2y^2+2x^2a^2+2y^2a^2-4x^2a^2}&=a^2
\\\sqrt{x^4+y^4+a^4+2x^2y^2-2x^2a^2+2y^2a^2}&=a^2
\\x^4+y^4+2x^2y^2&=2x^2a^2-2y^2a^2
\\(x^2+y^2)^2&=2a^2(x^2-y^2)
\end{aligned}
$$

**拓展变形**：定点在 $y$ 轴上时同理。

#### 顶点极值

> 双纽线上下四个顶点为 $(\pm\frac{\sqrt3}{2}a,\pm\frac{1}{2}a)$。

**评析**：可利用二次方程判别式，来求解其极值。

**证明**：

令直线 $l_1:y=t$，联立得 $x^4+t^4+2t^2x^2-2a^2x^2+2t^2a^2=0$。根据图像对称性可知，若交点存在，则必为一对或两对绝对值相等的值。用二次项 $k^2$ 换元四次项 $x^4$ 得 $k^2+t^4+2t^2k-2a^2k+2t^2a^2=0$，整理得 $k^2+(2t^2-2a^2)k+2t^2a^2+t^4=0$

换元后的方程仅有一个实根，则 $\Delta=0$，即：

$$
\begin{aligned}
(2t^2-2a^2)^2-4(2t^2a^2+t^4)&=0
\\4t^4-8a^2t^2+4a^4-8a^2t^2-4t^4&=0
\\a^4-4a^2t^2&=0
\\a^2-4t^2&=0
\\t&=\pm\frac{a}{2}
\end{aligned}
$$

反解得此时横坐标为 $\pm\frac{\sqrt3}{2}a$，即曲线的上顶点为 $(\pm\frac{\sqrt3}{2}a,\pm\frac{1}{2}a)$。同时不难发现其左右顶点为 $(\pm\sqrt2a,0)$。

证毕。

### 整点

> 在双纽线上，且横纵坐标均为整数的点叫做整点。

**评析**：首先根据上面给出的方法计算出顶点极值，接着在整数范围内套公式计算。

例如章头给出的双纽线 $(x^2+y^2)^2=18(x^2-y^2)$，结合上一节算出横纵坐标的取值范围 $x\in[-3\sqrt2,3\sqrt2],y\in[-\frac{3}{2},\frac{3}{2}]$。由于 $y$ 的范围较小，枚举 $y$ 方便些。$y=0$ 时，$(0,0),(\pm3\sqrt2,0)$ 在图像上，只有 $(0,0)$ 符合要求；$y=1$ 时，解方程 $x^4-16x^2+19=0$，换元可得 $x^2=8\pm3\sqrt5$，开根不可能得出整数。枚举完毕，整点仅 $(0,0)$。

切记不要忘记原点也在图像上。

## 带旋圆锥曲线 / 非标准型圆锥曲线

### 旋转变换

> 点 $P(x,y)$ 绕原点逆时针旋转 $\theta$ 角后的新坐标为 $P_1(x\cos\theta+y\sin\theta,-x\sin\theta+y\cos\theta)$，顺时针旋转 $\theta$ 角后的新坐标为 $P_2(x\cos\theta-y\sin\theta,x\sin\theta+y\cos\theta)$。

**评析**：如果你了解线性变换的相关知识，你就会知道这其实是乘旋转矩阵得到的结果。但如果你不知道，我们可以不用线性代数知识，现场推导一番。

**证明**：

![](https://cdn.luogu.com.cn/upload/image_hosting/3jy9okpe.png)

令 $P(x,y)$，假设 $OP$ 与 $x$ 轴正半轴所成角为 $\varphi$，那么 $x=|OP|\cos\varphi,y=|OP|\sin\varphi$，整理得 $\sin\varphi=\frac{y}{|OP|},\cos\varphi=\frac{x}{|OP|}$。由几何关系和旋转可得，$x_A=|OP|\cos(\varphi-\alpha),y_A=|OP|\sin(\varphi-\alpha)$。以 $x_A$ 推导为例：

$$
\begin{aligned}
x_A&=|OP|\cos(\varphi-\alpha)
\\&=|OP|(\cos\varphi\cos\alpha+\sin\varphi\sin\alpha)
\\&=|OP|\cos\varphi\cos\alpha+|OP|\sin\varphi\sin\alpha
\\&=|OP|\frac{x}{|OP|}\cos\alpha+|OP|\frac{y}{|OP|}\sin\alpha
\\&=x\cos\alpha+y\sin\alpha
\end{aligned}
$$

同理可得 $y_A=-x\sin\alpha+y\cos\alpha$，再如上算出 $B$ 点坐标，即证得成立。

证毕。

**拓展变形**：

如何将这一点运用到圆锥曲线上来呢？我们根据这个原理，联想到圆锥曲线的旋转本质上是将曲线上每一个点都做旋转变换，每个点的横纵坐标变换都满足如上规则。因此如果将圆锥曲线写成一个函数形式 $f(x,y)$，那么对应的逆时针旋转就是将函数变为 $f(x\cos\theta+y\sin\theta,-x\sin\theta+y\cos\theta)$，顺时针同理。

当然，旋转后的圆锥曲线与原圆锥曲线的形状是相同的。这意味着圆锥曲线的离心率等由其本身形状所决定的量不会发生改变，但是垂径定理、圆周定理将不再适用。


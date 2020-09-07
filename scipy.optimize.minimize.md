## Nelder-Mead

**1. Given a initial $x_0$ , generate $x_1 , ... , x_n$ . They are N-vector, and $x_i=x_0+0.05(x_0)_i$** 

​     根据一个初始点$x_0$生成一组初始数据 ${x_0,...,x_n}$, 这些点可以生成一个n维的单纯形.

   （二维的单纯形是个三角形，三维的单纯形是个四面体）

**2. Calculate $f(x_0), ... , f(x_n)$ , and reorder them. Then $m=\frac{1}{N}\sum^{n-1}_{0}x_i \ , \ r = m+\alpha (m-x_{n})$ **

​      计算这些点的函数值，并将它们从小到大重新排序.

​      计算除去最大值点外剩下点的中心 $m$ ,和最大值点关于此点的反射点$r = m+\alpha(m-x_{n})$

​       一般我们取上式中的 $\alpha$ 为1，反射点其实就是一个对称点.

​    **(1). If $f(x_0)\leq f(r)<f(x_{n-1})$ , let $x_{n}=r$** 

​    **(2). If $f(r)<f(x_0)$ , calculate $s=m+\beta(m-x_n)$ , let $x= r\text{ or } s$ , if $f(r \text{ or } s)$ is smaller.** 

​    **(3). If $f(x_{n-1}) \leq f(r) <f(x_n)$ , let $c_1 = m+\lambda (r-m)$,  and if $f(c_1)<f(r), x_n=c_1$, **

​           **or execute step 3.** 

​    **(4). If $f(x_n)\leq f(r)$, let $c_2 = m+\gamma (x_n-m)$, and if $f(c_2)<f(x_n)$, let $x_n=c_2$, or execute **

​           **step 3.**

​    以上 **step 2** 为循环体，因为我们要寻找最小值点，所以当前数据点里的最大值点要根据前面计算的$ m , r$不停地被替换，

​    四种不同情形看起来复杂，其核心思想就是让新点的函数值尽量小于当前的最大值点。在最差的情况，即新点只比当前

​    最大值点函数值小一点，甚至比当前最大函数值还要大，我们就执行 **step 3** 重新生成一组数据。最后直到满足精度要求

​    ，退出循环。（$\beta, \lambda, \gamma$ 的一般取值分别为：2，$\frac{1}{2}$，$\frac{1}{2}$）

**3. Let $v_i=x_0+\frac{(x_i-x_0)}{2}$ , and $x_i = v_i$**

#### Secant equation

$$
\nabla f=g_k-H_k(x-x_k)\\
\nabla f=g_{k-1}\\x=x_{k-1}\\
\Rightarrow g_{k-1}-g_k=H_k(x_{k-1}-x_k)
$$

#### Step Length

$$
min[f(x_k-\alpha \nabla f_k)]=\frac{1}{2}(x_k-\alpha \nabla f_k)^TQ(x_k-\alpha \nabla f_k)+b^T(x_k-\alpha \nabla f_k)
\\ \cases{\frac{\partial}{\part\alpha}f(x_k-\alpha \nabla f_k)=(x_k-\alpha \nabla f_k)^TQ\nabla f_k+b^T\nabla f_k=0 \\ \nabla f_k=Qx_k+b}
\\ \alpha=\frac{\nabla f_k^T\nabla f_k}{\nabla f_k^TQ\nabla f_k}
$$
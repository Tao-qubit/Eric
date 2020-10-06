# 11810416-陶贤哲-Assignment-1

## 6. 1

(a)
$$
\psi^0_n=\sqrt{\frac2a}\sin(\frac{n\pi x}a)\ ,\ H'=\alpha\delta(x-\frac a2) \\ 
\therefore E_n^1=\langle \psi_n^0|H'|\psi_n^0 \rangle=\frac{2\alpha}{a}\int^a_0\sin^2(\frac{n\pi x}a)\delta(x-\frac a2)dx=\frac{2\alpha}{a}\sin^2(\frac{n\pi}{2})\\
\therefore E_n^1=\cases{ 0\ \ \ \ \ \ \ \text{    for even  }n \\ \frac{2\alpha}{a}\ \ \ \ \ \text{ for odd }n}
$$
Because at $x=\frac{a}{2}$, $\psi_n^0=0$ for even $n$ , no perturbation can happen here

(b)
$$
c_m=\frac{\langle \psi_m^0|H'|\psi_n^0 \rangle}{E_n^0-E^0_m}
$$
For $n=1$ , first three nonzero terms are $m=3,5,7$
$$
\therefore c_3=\frac{\langle \psi_3^0|H'|\psi_1^0 \rangle}{E_1^0-E^0_3}=\frac{\frac{2\alpha}{a}\int\sin(\frac{3\pi x}{a})\delta(x-\frac a2)\sin(\frac{\pi x}{a})dx}{\frac{\pi^2\hbar^2}{2ma^2}(1^2-3^2)}=\frac{4ma\alpha}{\pi^2\hbar^2}\frac{1}{(3^2-1^2)}=\frac{ma\alpha}{2\pi^2\hbar^2}
$$
Likely
$$
c_5=-\frac{4ma\alpha}{\pi^2\hbar^2}\frac{1}{(5^2-1^2)}=-\frac{ma\alpha}{6\pi^2\hbar^2}\\
c_7=\frac{4ma\alpha}{\pi^2\hbar^2}\frac{1}{(7^2-1^2)}=\frac{ma\alpha}{12\pi^2\hbar^2}
$$
Therefore the three terms
$$
\psi_1^1=\frac{m\alpha}{\pi^2\hbar^2}\sqrt{\frac{a}{2}}[\sin(\frac{3\pi x}{a})-\frac{1}{3}\sin(\frac{5\pi x}{a})+\frac{1}{6}\sin(\frac{7\pi x}{a})+...]
$$

## 6. 3

(a)

The ground state is
$$
\psi_1^0(x_1,x_2)=\frac{2}{a}\sin(\frac{\pi x_1}{a})\sin (\frac{\pi x_2}a)
\\ E^0_1=\frac{(1^2+1^2)\pi^2\hbar^2}{2ma^2}=\frac{\pi^2\hbar^2}{ma^2}
$$
 The first excited state is
$$
\psi_2^0=\frac{\sqrt2}{a}[\sin(\frac{\pi x_1}{a})\sin(\frac{2\pi x_2}{a})+\sin(\frac{2\pi x_1}{a})\sin(\frac{\pi x_2}{a})]
\\ E_2^0=\frac{(1^2+2^2)\pi^2\hbar^2}{2ma^2}=\frac{5\pi^2\hbar^2}{2ma^2}
$$
(b)

The perturbation is
$$
V(x_1,x_2)=-aV_0\delta(x_1-x_2)
\\ E_1^1=\lang\psi^0_1 |H'|\psi_1^0) \rang=(-aV_0)(\frac{2}{a})^2\int\int\sin^2(\frac{\pi x_1}{a})\sin^2(\frac{\pi x_2}{a})\delta(x_1-x_2)dx_1dx_2\\=(-aV_0)(\frac{2}{a})^2\int_0^a\sin^4(\frac{\pi x_2}{a})dx_2=-\frac{3}{2}V_0
$$
Likely
$$
E^1_2=\lang\psi^0_2|H'|\psi^0_2\rang\\ = (-aV_0)(\frac{2}{a^2})\int\int[\sin(\frac{\pi x_1}{a})\sin(\frac{2\pi x_2}{a})+\sin(\frac{2\pi x_1}{a})\sin(\frac{\pi x_2}{a})]^2\delta(x_1-x_2)dx_1dx_2\\=-\frac{8V_0}{a}\int_0^a\sin^2(\frac{\pi x_2}{a})\sin^2(\frac{2\pi x_2}{a})dx_2
\\=-2V_0
$$

## 6. 5

$$
H'=-qEx
$$

(a)
$$
E^1_n=\lang\psi_n^0|H'|\psi_n^0\rang=-qE\lang\psi_n^0|x|\psi_n^0\rang=-qE\lang x \rang=0
$$
And
$$
E_n^0=(\frac12+n)\hbar\omega\\
E_n^2=\sum_{m\neq n}\frac{|\lang\psi_m^0|H'|\psi_n^0\rang|^2}{E^0_n-E^0_m}=q^2E^2\sum_{m\neq n}\frac{|\lang\psi_m^0|x|\psi_n^0\rang|^2}{\hbar\omega(n-m)}\\=\frac{q^2E^2}{2m\omega^2}\sum_{m\neq n}\frac{|\sqrt{n+1}\lang\psi_m^0|\psi_{n+1}^0\rang+\sqrt{n}\lang\psi^0_m|\psi^0_{n-1}\rang|^2}{n-m}\\ =\frac{q^2E^2}{2m\omega^2}[-(n+1)+n]=-\frac{q^2E^2}{2m\omega^2}
$$
(b)
$$
-\frac{\hbar^2}{2m}\frac{d^2\psi}{dx^2}+(\frac{1}{2}m\omega^2x^2-qEx)\psi=E\psi\\
$$
With the given change $x'$
$$
\frac{1}{2}m\omega^2x^2-qEx=\frac{1}{2}m\omega^2x'^2-\frac{1}{2}\frac{q^2E^2}{m\omega^2}\\
\therefore -\frac{\hbar^2}{2m}\frac{d^2\psi}{dx'^2}+(\frac{1}{2}m\omega^2x'^2-\frac{1}{2}\frac{q^2E^2}{m\omega^2})\psi=E\psi
\\\Rightarrow -\frac{\hbar^2}{2m}\frac{d^2\psi}{dx'^2}+\frac{1}{2}m\omega^2x'^2\psi=(E+\frac{1}{2}\frac{q^2E^2}{m\omega^2})\psi
\\ E_n+\frac{1}{2}\frac{q^2E^2}{m\omega^2}=(n+\frac{1}{2})\hbar\omega\\\therefore E_n=(n+\frac12)\hbar \omega-\frac12\frac{q^2E^2}{m\omega^2}
$$
We can see the second term is exactly what we got in (a), and higher corrections are zero

## 6. 7

$$
-\frac{\hbar^2}{2m}\frac{d^2\psi}{dx^2}=E\psi\\ \Rightarrow
\frac{d^2\psi}{dx^2}=-\frac{2mE}{\hbar^2}\psi=-k^2\psi
\\ \psi(x)=Ae^{ikx}+Be^{-ikx}
$$

And we have $\psi (x)=\psi(x+L)$
$$
Ae^{ikx}+Be^{-ikx}=Ae^{ik(x+L)}+Be^{-ik(x+L)}\\
\therefore \cases{Ae^{ikL}+Be^{-ikL}=A+B  \\Ae^{ikL}-Be^{-ikL}=A-B}\\
\therefore 2A e^{ikL}=2A  \Rightarrow k=\frac{2n\pi}{L}
$$
And normalization gives that $A=\frac{1}{\sqrt L}$ , so we get
$$
\psi_n(x)=\frac{1}{\sqrt L}e^{\frac{i(2n\pi x)}{L}}\\
E_n=\frac{2n^2\pi^2\hbar^2}{mL^2}
$$
(b)
$$
H'=-V_0e^{-\frac{x^2}{a^2}}\\
\\\therefore W_{aa}= W_{bb}=-\frac{V_0}{L}\int^{\infty}_{-\infty}e^{-\frac{x^2}{a^2}}dx =-\frac {V_0} {L}a\sqrt{\pi}\\ W_{ab}=-\frac{V_0}{L}\int^{\infty}_{-\infty}e^{-\frac{x^2}{a^2}+\frac{i(4n\pi x)}{L}}dx=-\frac{V_0}{L}a\sqrt\pi e^{-\frac{4n^2\pi^2a^2}{L^2}} \\
\Rightarrow E^1_{\pm}=\frac12[W_{aa}+W_{bb}\pm\sqrt{(W_{aa}-W_{bb})^2+4|W_{ab}|^2}]=-\frac{aV_0}{L}\sqrt{\pi}(1\mp e^{-\frac{4n^2\pi^2a^2}{L^2}})
$$
(c)
$$
\beta=\frac{E_\pm^1-W_{bb}}{W_{ba}}\alpha=\frac{\mp e^{-\frac{4n^2\pi^2a^2}{L^2}}}{e^{-\frac{4n^2\pi^2a^2}{L^2}}}=\mp\alpha
\\ \therefore \psi_+=\alpha\psi_n-\alpha\psi_{-n}=i\sqrt{\frac{2}{L}}\sin(\frac{2n\pi x}{L})\\ \psi_-=\alpha\psi_n+\alpha\psi_{-n}=\sqrt{\frac{2}{L}}\cos(\frac{2n\pi x}{L})\\
E_+^1=\lang \psi_+ |H'|\psi_+\rang=-\frac{aV_0}{L}\sqrt{\pi}(1- e^{-\frac{4n^2\pi^2a^2}{L^2}})\\
E_-^1=\lang \psi_- |H'|\psi_-\rang=-\frac{aV_0}{L}\sqrt{\pi}(1+ e^{-\frac{4n^2\pi^2a^2}{L^2}})
$$
(d)

Consider that
$$
Af(x)=f(-x)\\ 
$$
And $\psi_+$ is an odd function, $\psi_-$ is an even function, so
$$
\therefore A\psi_+=-\psi_+\\
A\psi_-=\psi_-
$$
Therefore $\psi_+ , \psi_-$ are $A$'s eigenfunctions for eigenvalues $-1$ and $1$

## 6. 9

(a)

Without perturbation
$$
H=V_0\left(  \matrix{1\ \ \ 0\ \ \ 0\\0\ \ \ 1\ \ \ 0\\0\ \ \ 0\ \ \ 2}\right)
$$
The eigenvalues $\chi$ and eigenvector $E^0$ are
$$
\chi_1=\left(  \matrix{1\\0\\0}\right)\text{ for }E^0_1=V_0  \\
\chi_2=\left(  \matrix{0\\1\\0}\right)\text{ for }E^0_2=V_0\\
\chi_3=\left(  \matrix{0\\0\\1}\right)\text{ for }E_3^0=2V_0
$$
(b)

With perturbation

$$
\begin{aligned}H-\lambda I=\left(  \matrix{&V_0(1-\epsilon)-\lambda &0 &0&\\&0 &V_0-\lambda &\epsilon V_0&\\&0 &\epsilon V_0 &2V_0-\lambda&}\right)\end{aligned}
$$
Let $\det (H-\lambda I)=0$
$$
[V_0(1-\epsilon)-\lambda][(V_0-\lambda)(2V_0-\lambda)-V_0^2\epsilon^2]=0
\\ [V_0(1-\epsilon)-\lambda][\lambda^2-3V_0\lambda+(2-\epsilon^2)V_0^2]=0
$$
Solution is
$$
\lambda_1=(1-\epsilon)V_0\\
\lambda_2=\frac{3-\sqrt{1+4\epsilon^2}}{2}V_0\approx(1-\epsilon^2)V_0\\
\lambda_3=\frac{3+\sqrt{1+4\epsilon^2}}{2}V_0\approx(2+\epsilon^2)V_0
$$
(c)
$$
\begin{aligned}H'=\epsilon V_0\left(  \matrix{-1 &0 &0\\0 &0 &1\\0 &1 &0}\right)\end{aligned}
$$
And $\chi_3$ is not degenerate
$$
E^1_3=\lang \chi_3|H'|\chi_3\rang=\epsilon V_0\begin{aligned}\left(\matrix{0&0&1}\right)\left(  \matrix{-1 &0 &0\\0 &0 &1\\0 &1 &0}\right)\left(  \matrix{0\\0\\1}\right)\end{aligned}=0 \\
E^2_3=\sum^2_{n=1}\frac{|\lang\chi_3^0|H'|\chi_n^0\rang|^2}{E_3^0-E^0_n}=0+\frac{V^2_0\epsilon^2}{V_0}=V_0\epsilon^2
$$

Therefore
$$
E_3=E_3^0+E_3^1+E^2_3=2V_0+0+V_0\epsilon^2=(2+\epsilon^2)V_0
$$
The result is the same as what we got before

(d)

$$
W_{11}=\lang\chi_1|H'|\chi_1\rang=-\epsilon V_0\\
W_{22}=\lang\chi_2|H'|\chi_2\rang=0\\
W_{12}=W_{21}=\lang\chi_1|H'|\chi_2\rang=0
$$
Then
$$
E^1_{\pm}=\frac12\left[(W_{11}+W_{22})\pm\sqrt{(W_{11}-W_{22})^2+4|W_{12}|^2}\right]
\\\Rightarrow\cases{E^1_+=0\\E^1_-=-\epsilon V_0}
$$
Therefore
$$
E_1=E_1^0+E^1_{+}=V_0\\
E_2=E_2^0+E_-^1=(1-\epsilon)V_0
$$
The result is consistent with (b) up to the first order

## 6. 14

$$
H'=-\frac{3p^4}{8m^3c^2}\\
\Rightarrow E^1_r=-\frac1{2mc^2}[E^2-2E\lang V\rang+\lang V^2 \rang]
$$

And for harmonic oscillator
$$
E=(n+\frac{1}{2})\hbar\omega \ , \ V=\frac12m\omega^2x^2
\\ \Rightarrow E^1_r=-\frac{1}{2mc^2}[(n+\frac12)^2\hbar^2\omega^2-(n+\frac12)\hbar m \omega^3\lang x^2 \rang+\frac14m^2\omega^4\lang x^4 \rang]
$$
Use $x=\sqrt{\frac{\hbar}{2m\omega}}(a_++a_-) , p=i\sqrt{\frac{\hbar m\omega}{2}}(a_+-a_-)$
$$
\lang x^2 \rang=(n+\frac12)\frac{\hbar}{m\omega}\\
\lang x^4\rang=[n(n-1)+(n+2)(n+1)+n^2+n(n+1)+n(n+1)+(n+1)^2]\frac{\hbar^2}{4m^2\omega^2}\\=(6n^2+6n+3)\frac{\hbar^2}{4m^2\omega^2}
$$
Therefore
$$
E_r^1=-\frac{1}{2mc^2}[(n+\frac12)^2\hbar^2\omega^2-(n+\frac12)^2\hbar ^2\omega^2+\frac{6n^2+6n+3}{16}\hbar^2\omega^2]\\
=-\frac{6n^2+6n+3}{32}\frac{\hbar^2\omega^2}{mc^2}
$$

## 6. 16

(a)
$$
[L\cdot S,L_x]=[L_xS_x+L_yS_y+L_zS_z,L_x]=[L_x,L_x]S_x+[L_y,L_x]S_y+[L_z,L_x]S_z
\\=0S_x-i\hbar L_zS_y+i\hbar L_yS_z\\
=i\hbar(L_yS_z-L_zS_y)=i\hbar(L\times S)_x
$$
Similarly, $[L\cdot S,L_y]=i\hbar(L\times S)_y , [L\cdot S,L_z]=i\hbar(L\times S)_z$

Therefore $[L\cdot S,L]=i\hbar(L\times S)$

(b)

$$
[L\cdot S,S_x]=[L_xS_x+L_yS_y+L_zS_z,S_x]=[S_x,S_x]L_x+[S_y,S_x]L_y+[S_z,S_x]L_z
\\=0L_x-i\hbar S_zL_y+i\hbar S_yL_z\\
=i\hbar(S_yL_z-S_zL_x)=i\hbar(S\times L)_x
$$
Similarly, $[L\cdot S,S_y]=i\hbar(S\times L)_y , [L\cdot S,L_z]=i\hbar(S\times L)_z$

Therefore $[L\cdot S,S]=i\hbar(S\times L)$

(c)
$$
[L\cdot S,J]=[L\cdot S,L]+[L\cdot S,S]=i\hbar(L\times S+S\times L)=0
$$
(d)
$$
[L\cdot S,L^2]=[L_xS_x+L_yS_y+L_zS_z,L_xL_x+L_yL_y+L_zL_z]
$$
For each term
$$
[L_iS_i,L_jL_j]=L_j[L_i,L_j]S_i+[L_i,L_j]L_jS_i\\
i,j\in \{x,y,z\}
$$
And
$$
\sum_{j\in\{x,y,z\}}(L_j[L_x,L_j]S_x+[L_x,L_j]L_jS_x)=i\hbar (L_yL_zS_x+L_zL_yS_x-L_zL_yS_x-L_yL_zS_x)=0\\
\Rightarrow \sum_{i\in\{x,y,z\}}\sum_{{j\in\{x,y,z\}}}[L_iS_i,L_jL_j]=0+0+0=0
$$
Therefore
$$
[L\cdot S,L^2]=0
$$
(e)
$$
[L\cdot S,S^2]=[L_xS_x+L_yS_y+L_zS_z,S_xS_x+S_yS_y+S_zS_z]
$$
For each term
$$
[L_iS_i,S_jS_j]=L_i[S_i,S_j]S_j+L_iS_j[S_i,S_j]\\
i,j\in \{x,y,z\}
$$
And
$$
\sum_{j\in\{x,y,z\}}(L_x[S_x,S_j]S_j+L_xS_j[S_x,S_j])=i\hbar (L_xS_zS_y+L_xS_yS_z-L_xS_yS_z-L_xS_zS_y)=0\\
\Rightarrow \sum_{i\in\{x,y,z\}}\sum_{{j\in\{x,y,z\}}}[L_iS_i,S_jS_j]=0+0+0=0
$$
Therefore
$$
[L\cdot S,S^2]=0
$$
(f)
$$
[L\cdot S,J^2]=[L\cdot S,L^2]+[L\cdot S,S^2]+2[L\cdot S,L\cdot S]=0+0+0=0
$$

## 6. 17

We know that
$$
E^1_r=-\frac{(E_n)^2}{mc^2}\left(\frac{2n}{l+\frac12}-\frac32\right)\\
E^1_{so}=\frac{(E_n)^2}{mc^2}\left[\frac{nj(j+1)-nl(l+1)-\frac34n}{l(l+\frac12)(l+1)}\right]
$$
Use $j=l+\frac12$
$$
E^1_r=-\frac{(E_n)^2}{mc^2}\left(\frac{2n}{j}-\frac32\right)\\
E^1_{so}=\frac{(E_n)^2}{mc^2}\left[\frac{nj(j+1)-n(j-\frac12)(j+\frac12)-\frac34n}{j(j-\frac12)(j+\frac12)}\right]=\frac{(E_n)^2}{mc^2}\left[\frac{n}{j(j+\frac12)}\right]
$$
Thus
$$
E^1_{fs}=E^1_r+E_{so}^1=\frac{(E_n)^2}{mc^2}\left(-\frac{2n}{j+\frac12}+\frac32\right)=\frac{(E_n)^2}{2mc^2}\left(3-\frac{4n}{j+\frac12}\right)
$$

Use $j=l-\frac12$
$$
E^1_r=-\frac{(E_n)^2}{mc^2}\left(\frac{2n}{j+1}-\frac32\right)\\
E^1_{so}=\frac{(E_n)^2}{mc^2}\left[\frac{nj(j+1)-n(j+\frac12)(j+\frac32)-\frac34n}{(j+\frac12)(j+1)(j+\frac32)}\right]=-\frac{(E_n)^2}{mc^2}\frac{n}{(j+\frac12)(j+1)}
$$
Thus
$$
E^1_{fs}=E^1_r+E_{so}^1=-\frac{(E_n)^2}{mc^2}\left(\frac{2n}{j+\frac12}-\frac32\right)=\frac{(E_n)^2}{2mc^2}\left(3-\frac{4n}{j+\frac12}\right)
$$
Therefore
$$
E^1_{fs}=E^1_r+E_{so}^1=\frac{(E_n)^2}{2mc^2}\left(3-\frac{4n}{j+\frac12}\right)
$$

## 6. 21













































































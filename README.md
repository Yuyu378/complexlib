# complexlib
Complex Arithmetic Library of C

## Proof of complex arithmetic  
### Power
#### Case 1
$$
\begin{align}
    (A+Bi)^{\ n}
        &= (r\ e^{\ i\varphi})^{\ n} \\
        &= r^{\ n}\ e^{\ i\ n\varphi} \\
        &= r^{\ n}\ (\cos n\varphi\ +\ i\sin n\varphi)\qquad\qquad\qquad\qquad\qquad\qquad\qquad
\end{align}
$$  

#### Case 2
$$
\begin{align}
    A^{\ a\ +\ bi}
        &= A^a\ A^{bi} \\
        &= A^a\ e^{\ln{\hspace{-0.2em}A^{bi}}} \\
        &= A^a\ e^{\ i\ b\ln{\hspace{-0.2em}A}} \\
        &=
    \begin{cases}
        \ A^a\ (\cos{\ b\ln{\hspace{-0.2em}A}} + i\sin{\ b\ln{\hspace{-0.2em}A}}) 
            & \quad\hspace{0.6em}\qquad A > 0 \\
        \ nan 
            & \quad\text{if}\qquad A = 0 \\
        \ A^a\ e^{-\pi b}\ (\cos{\ b\ln{\hspace{-0.2em}\vert A\vert}} + i\sin{\ b\ln{\hspace{-0.2em}\vert A\vert}})
            & \quad\hspace{0.6em}\qquad A < 0 
    \end{cases}
\end{align}
$$

#### Case 3
$$
\begin{align}		
    (A+Bi)^{\ a\ +\ bi} 
        &= (r\ e^{\ i\varphi})^{a\ +\ bi} \\
        &= (r\ e^{\ i\varphi})^{a}\ (r\ e^{\ i\varphi})^{bi} \\
        &= r^{\ a}\ e^{\ ia\varphi}\ r^{\ bi}\ e^{-b\varphi} \\
        &= r^{\ a}\ (\cos{a\varphi}\ +\ i\sin{a\varphi})\ e^{\ \ln{r^{\ bi}} }\ e^{-b\varphi} \\
        &= r^{\ a}\ (\cos{a\varphi}\ +\ i\sin{a\varphi})\ e^{\ i\ b\hspace{-0.05em}\ln\hspace{-0.05em}r}\ e^{-b\varphi} \\
        &= r^{\ a}\ (\cos{a\varphi}\ +\ i\sin{a\varphi})\ (\cos{b}\hspace{-0.05em}\ln\hspace{-0.05em}r\ +\ i\sin{b}\hspace{-0.05em}\ln\hspace{-0.05em}r)\ e^{-b\varphi}\qquad\qquad
\end{align}
$$
****
### Exponential
$$
\begin{align}
    e^{(A+Bi)}
        &= e^{\ A}\ e^{\ iB} \\
        &= e^{\ A}\ (\cos{B}\ +\ i\sin{B})
\end{align}
$$
****
### Logarithm
#### Case 1
$$
\begin{align}
    \log_n{(A+Bi)}
    	&= \log_n{(r\ e^{\ i\varphi})} \\
        &= \frac{\ \ln{(r\ e^{\ i\varphi}) }\ }{ \ln{n} } \\
        &= \frac{\ \ln{r}\ +\ \ln{e^{\ i\varphi} }\ }{ \ln{n} } \\
        &= \frac{\ \ln{r}\ +\ i\varphi\ }{ \ln{n} }
\end{align}
$$

#### Case 2
$$
\begin{align}
    \log_{(a+bi)}{(A+Bi)}
    	&= \log_{(\gamma\ e^{\ i\theta})}{(r\ e^{\ i\varphi})} \\
        &= \frac{\ \ln{(r\ e^{\ i\varphi}) }\ }{ \ln{(\gamma\ e^{\ i\theta})} } \\
        &= \frac{\ \ln{r}\ +\ \ln{\ e^{\ i\varphi} }\ }{ \ln{\gamma}\ +\ \ln{\ e^{\ i\theta} } } \\
        &= \frac{\ \ln{r}\ +\ i\varphi\ }{ \ln{\gamma}\ +\ i\theta }
\end{align}
$$
****
### Trigonometry
#### Common Functions
$$
\begin{align}
    \sin{(A+Bi)}
    	&= \frac{\ e^{i(A+Bi)}\ -\ e^{-i(A+Bi)}\ }{2i} \\
        &= \frac{\ e^{(-B+Ai)}\ -\ e^{(B-Ai)}\ }{2i} \\
        &= \frac{\ e^{-B}\ e^{iA}\ -\ e^{B}\ e^{-iA}\ }{2i} \\
        &= \frac{\ e^{-B}\ (\cos{A}\ +\ i\sin{A})\ -\ e^{B}\ (\cos{A}\ -\ i\sin{A})\ }{2i} \\
    \\
    \cos{(A+Bi)}
    	&= \frac{\ e^{i(A+Bi)}\ +\ e^{-i(A+Bi)}\ }{2} \\
        &= \frac{\ e^{-B}\ (\cos{A}\ +\ i\sin{A})\ +\ e^{B}\ (\cos{A}\ -\ i\sin{A})\ }{2} \\
    \\
    \tan{(A+Bi)}
    	&= \frac{\sin{(A+Bi)}}{\cos{(A+Bi)}} \\
        &= -i\frac{\ e^{i(A+Bi)}\ -\ e^{-i(A+Bi)}\ }{\ e^{i(A+Bi)}\ +\ e^{-i(A+Bi)}\ } \\
        &= \frac{\ e^{-B}\ (\sin{A}\ -\ i\cos{A})\ +\ e^{B}\ (\sin{A}\ +\ i\cos{A})\ }{\ e^{-B}\ (\cos{A}\ +\ i\sin{A})\ +\ e^{B}\ (\cos{A}\ -\ i\sin{A})\ }
\end{align}
$$

#### Arcsine
$$
\begin{align}
    \text{Let }\quad \omega &= \alpha + \beta i\ ,\quad v = e^{i\omega} \\
    \\
    z   &= A + Bi = \sin{\omega} = \frac{\ v\ -\ v^{-1}\ }{2i} \\
    \\
    \text{Thus }\quad & v^2 - 2izv - 1 = 0 \\
    \\
    v   &= \frac{2iz\pm\sqrt{-4z^2 + 4}}{2} \\
        &= iz\pm\sqrt{1 - z^2} \\
        &= iz\pm e^{\ln{ {(1 - z^2)} ^{\frac{1}{2}}}} \\
    \\
    \text{Euler's} & \text{ formula } \quad 1 - z^2 = \zeta e^{i\vartheta} \\
    \\
    v   &= iz\pm e^{\frac{1}{2}\ln{ \zeta e^{i\vartheta} }} \\
        &= iz\pm e^{\frac{1}{2}(\ln{\zeta} + \ln{e^{i\vartheta}})} \\
        &= iz\pm e^{\ln{ {\zeta}^{\frac{1}{2}} }}e^{i\frac{\vartheta}{2}} \\
        &= iz\pm \sqrt{\zeta}\ (\cos{\frac{\vartheta}{2}}\ +\ i\sin{\frac{\vartheta}{2}}) \\
    \\
    w   &= \frac{1}{i}\ln{v} \\
        &= -i\ln{ \begin{Bmatrix} iz\pm \sqrt{\zeta}\ (\cos{\frac{\vartheta}{2}}\ +\ i\sin{\frac{\vartheta}{2}}) \end{Bmatrix} } \\
    \\
    \\
    \sin^{-1}(z) = -i\ln
        & \begin{Bmatrix}iz\pm\sqrt{\vert 1-z^2\vert}\ \left(\cos{\frac{\text{Arg}(1-z^2)}{2}}\ +\ i\sin{\frac{\text{Arg}(1-z^2)}{2}}\right) \end{Bmatrix}
\end{align}
$$

#### Arccosine
$$
\begin{align}
    \text{Let }\quad \omega &= \alpha + \beta i\ ,\quad v = e^{i\omega} \\
    \\
    z   &= A + Bi = \sin{\omega} = \frac{\ v\ +\ v^{-1}\ }{2} \\
    \\
    \text{Thus }\quad & v^2 - 2zv + 1 = 0 \\
    \\
    v   &= \frac{2z\pm\sqrt{4z^2 - 4}}{2} \\
        &= z\pm\sqrt{z^2 - 1} \\
        &= z\pm e^{\ln{ {(z^2 - 1)} ^{\frac{1}{2}}}} \\
    \\
    \text{Euler's} & \text{ formula } \quad z^2 - 1 = \zeta e^{i\vartheta} \\
    \\
    v   &= z\pm e^{\frac{1}{2}\ln{ \zeta e^{i\vartheta} }} \\
        &= z\pm e^{\frac{1}{2}(\ln{\zeta} + \ln{e^{i\vartheta}})} \\
        &= z\pm e^{\ln{ {\zeta}^{\frac{1}{2}} }}e^{i\frac{\vartheta}{2}} \\
        &= z\pm \sqrt{\zeta}\ (\cos{\frac{\vartheta}{2}}\ +\ i\sin{\frac{\vartheta}{2}}) \\
    \\
    w   &= \frac{1}{i}\ln{v} \\
        &= -i\ln{ \begin{Bmatrix} z\pm \sqrt{\zeta}\ (\cos{\frac{\vartheta}{2}}\ +\ i\sin{\frac{\vartheta}{2}}) \end{Bmatrix} } \\
    \\
    \\
    \cos^{-1}(z) = -i\ln
        & \begin{Bmatrix}z\pm\sqrt{\vert z^2-1\vert}\ \left(\cos{\frac{\text{Arg}(z^2-1)}{2}}\ +\ i\sin{\frac{\text{Arg}(z^2-1)}{2}}\right) \end{Bmatrix}
\end{align}
$$

#### Arctangent
$$
\begin{align}
    \text{Let }\quad \omega &= \alpha + \beta i \\
    \\
    z   &= A + Bi = \tan{\omega} = \frac{\hspace{0.15em}\sin\omega}{\ \cos\omega\ } = \frac{1}{i}\frac{e^{i\omega}-e^{-i\omega}}{\ e^{i\omega}+e^{-i\omega}\ } \\
    \\
    iz  &= \frac{e^{i\omega}-e^{-i\omega}}{\ e^{i\omega}+e^{-i\omega}\ } = \frac{e^{i2\omega}-1}{\ e^{i2\omega}+1\ }\\
    \\
    e^{i2\omega}
        &= \frac{iz+1}{\ 1-iz\ } = \frac{i-z}{\ i+z\ } \\
    \\
    w   &= \frac{1}{2i}\ln\frac{i-z}{\ i+z\ } \\
    \\
    \text{Euler's} & \text{ formula } \quad \frac{i-z}{\ i+z\ } = \zeta e^{i\vartheta} \\
    \\
    w   &= \frac{1}{2i}\ln{\zeta e^{i\vartheta}} \\
        &= \frac{1}{2i}(\ln\zeta + \ln{e^{i\vartheta}}) \\
        &= \frac{1}{2i}(\ln\zeta + i\vartheta) \\
    \\
    \\
    \tan^{-1}(z)
        &= -\frac{i}{2}\begin{Bmatrix}\ \ln{\left\vert\large\frac{i-z}{\ i+z\ }\right\vert} + i\text{Arg}\left(\large\frac{i-z}{\ i+z\ }\right)\ \end{Bmatrix}
\end{align}
$$

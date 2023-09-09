# complexlib
Complex Arithmetic Library of C

## Proof of complex arithmetic  
### Power
#### case 1
$$
\begin{align}
    (A+Bi)^{\ n}
        &= (r\ e^{\ i\varphi})^{\ n} \\
        &= r^{\ n}\ e^{\ i\ n\varphi} \\
        &= r^{\ n}\ (\cos n\varphi\ +\ i\sin n\varphi)
\end{align}
$$  

#### case 2
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

#### case 3
$$
\begin{align}		
    (A+Bi)^{\ a\ +\ bi} 
        &= (r\ e^{\ i\varphi})^{a\ +\ bi} \\
        &= (r\ e^{\ i\varphi})^{a}\ (r\ e^{\ i\varphi})^{bi} \\
        &= r^{\ a}\ e^{\ ia\varphi}\ r^{\ bi}\ e^{-b\varphi} \\
        &= r^{\ a}\ (\cos{a\varphi}\ +\ i\sin{a\varphi})\ e^{\ \ln{r^{\ bi}} }\ e^{-b\varphi} \\
        &= r^{\ a}\ (\cos{a\varphi}\ +\ i\sin{a\varphi})\ e^{\ i\ b\hspace{-0.05em}\ln\hspace{-0.05em}r}\ e^{-b\varphi} \\
        &= r^{\ a}\ (\cos{a\varphi}\ +\ i\sin{a\varphi})\ (\cos{b}\hspace{-0.05em}\ln\hspace{-0.05em}r\ +\ i\sin{b}\hspace{-0.05em}\ln\hspace{-0.05em}r)\ e^{-b\varphi} \\
\end{align}
$$

### Exponential
$$
\begin{align}
    e^{(A+Bi)}
        &= e^{\ A}\ e^{\ iB} \\
        &= e^{\ A}\ (\cos{B}\ +\ i\sin{B})
\end{align}
$$

### Logarithm
#### case 1
$$
\begin{align}
    \log_n{(A+Bi)}
    	&= \log_n{(r\ e^{\ i\varphi})} \\
        &= \frac{\ \ln{(r\ e^{\ i\varphi}) }\ }{ \ln{n} } \\
        &= \frac{\ \ln{r}\ +\ \ln{e^{\ i\varphi} }\ }{ \ln{n} } \\
        &= \frac{\ \ln{r}\ +\ i\varphi\ }{ \ln{n} }
\end{align}
$$

#### case 2
$$
\begin{align}
    \log_{(a+bi)}{(A+Bi)}
    	&= \log_{(\gamma\ e^{\ i\theta})}{(r\ e^{\ i\varphi})} \\
        &= \frac{\ \ln{(r\ e^{\ i\varphi}) }\ }{ \ln{(\gamma\ e^{\ i\theta})} } \\
        &= \frac{\ \ln{r}\ +\ \ln{\ e^{\ i\varphi} }\ }{ \ln{\gamma}\ +\ \ln{\ e^{\ i\theta} } } \\
        &= \frac{\ \ln{r}\ +\ i\varphi\ }{ \ln{\gamma}\ +\ i\theta }
\end{align}
$$

### Trigonometry
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

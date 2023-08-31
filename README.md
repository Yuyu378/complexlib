# complexlib
Complex Arithmetic Library of C

# Proof of complex arithmetic

### Power
> #### case 1 
$$
\begin{aligned}
    (A+Bi)^{\ n}
        &= (r\ e^{\ i\varphi})^{\ n} \\
        &= r^{\ n}\ e^{\ i\ n\varphi} \\
        &= r^{\ n}\ (\cos n\varphi\ +\ i\sin n\varphi)\hspace{15.5em}
\end{aligned}
$$

> #### case 2
$$
\begin{aligned}
    A^{\ a\ +\ bi}
        &= A^{\ a}\ A^{\ bi} \\
        &= A^{\ a}\ e^{\ \ln A^{bi}} \\
        &= A^{\ a}\ e^{\ i\ b\hspace{-0.05em}\ln\hspace{-0.1em}A} \\
        &=
    \begin{cases}
        \ A^{\ a}\ (\cos\ b\ln\hspace{-0.1em}A + i\sin\ b\ln\hspace{-0.1em}A) 
            & \quad\hspace{0.6em}\qquad A > 0 \\
        \ nan 
            & \quad\text{if}\qquad A = 0 \\
        \ A^{\ a}\ e^{-\pi b}\ (\cos\ b\ln\hspace{-0.1em}\vert A\vert + i\sin\ b\ln\hspace{-0.1em}\vert A\vert)
            & \quad\hspace{0.6em}\qquad A < 0 
    \end{cases}
\end{aligned}
$$

> #### case 3
$$
\begin{aligned}		
    (A+Bi)^{\ a\ +\ bi} 
        &= (r\ e^{\ i\varphi})^{\ a\ +\ bi} \\
	    &= (r\ e^{\ i\varphi})^{\ a}\ (r\ e^{\ i\varphi})^{\ bi} \\
        &= r^{\ a}\ e^{\ i\ a\varphi}\ r^{\ bi}\ e^{\ -b\varphi} \\
        &= r^{\ a}\ (\cos a\varphi\ +\ i\sin a\varphi)\ e^{\ \ln r^{\ bi}}\ e^{\ -b\varphi} \\
        &= r^{\ a}\ (\cos a\varphi\ +\ i\sin a\varphi)\ e^{\ i\ b\hspace{-0.05em}\ln\hspace{-0.05em}r}\ e^{\ -b\varphi} \\
        &= r^{\ a}\ (\cos a\varphi\ +\ i\sin a\varphi)\ (\cos b\hspace{-0.05em}\ln\hspace{-0.05em}r\ +\ i\sin b\hspace{-0.05em}\ln\hspace{-0.05em}r)\ e^{\ -b\varphi}\hspace{5em} \\
\end{aligned}
$$

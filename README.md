# General Circuit
![](Pasted%20image%2020250715105507.png)

# Analysis
From KCL at the $V_p$ node, we get $$v_x = v_{out}[1 + \frac{Z_2}{Z_3}]$$

Solving KCL at the $v_x$ node, we get the transfer function as $$H(s) = \frac{Z_3Z_4}{Z_1Z_2 + Z_1Z_4 + Z_2Z_4 + Z_3Z_4}$$

The general equation for a second order high-pass filter is $$\frac{-Ks^2}{-s^2+\frac{s}{Q} + 1}$$

On configuring the impedances for a general high-pass circuit with $Z_1 = \frac{1}{sC_1}, Z_2 = \frac{1}{sC_2}$ and $Z_3 = R_1, Z_4 = R_2$ we get the transfer function

$$\frac{s^2(R_1R_2C_1C_2)}{s^2(R_1R_2C_1C_2)+s(R_2C_2 + R_2C_1) + 1}$$

To simplify calculations, we set $R_1 = R_2$ and $C_1 = C_2$, and we get $f_0 = \frac{1}{2\pi RC}$, and $Q = \frac{1}{2}$.

This quality factor is sometimes not enough, so we will now use resistors $R_3$ and $R_4$ to attenuate the negative feedback, which will result in the output increasing in compensation.
![](Pasted%20image%2020250715113409.png)

# Simulation
After performing a similar analysis, we see that $f_c$ is unchanged but Q is now $\frac{1}{3-K}$, where K is $1+\frac{R_4}{R_3}$. 


![](Pasted%20image%2020250715120102.png)
![](Pasted%20image%2020250715120047.png)

---
layout: page
title: Mass-Energy Equivalence
importance: 2
category: derivations
---

The assumptions of special relativity lead to the most famous equation in physics: $$ E=mc^2$$. It derives naturally from the assumption that the speed of light is the same in all frames of reference.
Starting from the definition of Kinetic energy:

$$ 
\begin{align*}
\frac{dK}{dt} = v\frac{dp}{dt} = vm\frac{d}{dt}(\gamma v)
\end{align*}
$$

Where we have used the relativistic momentum: $$ p =  \gamma mv $$, and $$\gamma = (1-v^2/c^2)^{-1/2}$$ is the <a href="https://en.wikipedia.org/wiki/Lorentz_factor" target=_blank >Lorentz factor</a>:

$$
\begin{align*}
\frac{d(\gamma v)}{dt} &= \frac{d}{dt} \frac{v}{\sqrt{1-v^2/c^2}} \\
&= \Bigg[\Bigg(1 - \frac{v^2}{c^2}\Bigg)^{-1/2} + \frac{v^2}{c^2} \Bigg(1 - \frac{v^2}{c^2}\Bigg)^{-3/2}\Bigg] \frac{dv}{dt} \\
&= \Bigg[\Bigg(1 - \frac{v^2}{c^2}\Bigg)^{-1/2}\Bigg\{1 + \frac{v^2}{c^2} \Bigg(1 - \frac{v^2}{c^2}\Bigg)^{-1} \Bigg\} \Bigg] \frac{dv}{dt}\\
&= \Bigg[\Bigg(1 - \frac{v^2}{c^2}\Bigg)^{-1/2}\Bigg\{\frac{1 -v^2/c^2}{1 -v^2/c^2} +  \frac{v^2/c^2}{1 -v^2/c^2}\Bigg\} \Bigg] \frac{dv}{dt}\\
&= \Bigg(1 - \frac{v^2}{c^2}\Bigg)^{-3/2} \frac{dv}{dt}
\end{align*}
$$

Hence:

$$
\begin{align*}
\frac{dK}{dt} &= m\Bigg(1 - \frac{v^2}{c^2}\Bigg)^{-3/2} v\frac{dv}{dt} \\
&= \frac{d}{dt} \frac{m c^2}{\sqrt{1-v^2/c^2}} = \frac{d}{dt} \Big(\gamma m c^2\Big)
\end{align*}
$$

Where we have used the fact that: 

$$
\begin{align*}
\frac{d}{dt} \frac{c^2}{\sqrt{1-v^2/c^2}} = \Big(1 - \frac{v^2}{c^2}\Big)^{-3/2} v\frac{dv}{dt}
\end{align*}
$$

Integrating both sides, knowing that the kinetic energy is zero at rest ($$\gamma=1$$ when $$v=0$$), we get:

$$
\begin{align*}
K &= \gamma m c^2 + C \\
&= \gamma m c^2 - mc^2
\end{align*}
$$

We can  recover the classic Newtonian kinetic energy $$ K = \frac{1}{2} m v^2$$ by taking $$v<<c$$:

$$
\begin{align*}
K &= \gamma m c^2 - mc^2 \\
&= mc^2\Bigg(\frac{1}{\sqrt{1-v^2/c^2}} - 1\Bigg) \\
&= mc^2\Bigg(1 + \frac{1}{2} \frac{v^2}{c^2} + ... - 1\Bigg) \\
&\approx \frac{1}{2} m v^2
\end{align*}
$$

We can interpret $$K= \gamma m c^2 - mc^2$$ as $$K = T - E$$ where $$T$$ is the total energy and $$E$$ is the rest energy. Hence, we have:

$$E = m c^2 $$



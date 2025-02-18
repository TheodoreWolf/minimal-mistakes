---
layout: page
title: The integral of the Gaussian distribution
importance: 2
category: derivations
---

This one is just beautiful, links $$\pi$$ and $$e$$ together even though they really don't seem related.

$$
\begin{align*}
  \int{e^{-x^2} dx} &= \sqrt{\int{e^{-x^2} dx} \int{e^{-x^2} dx}} \\
\end{align*}
$$

Switching to a dummy variable:

$$
\begin{align*}
    &=  \sqrt{\int{e^{-x^2} dx} \int{e^{-y^2} dy}} \\
    &= \sqrt{\int\int{e^{-(x^2 + y^2)} dx\, dy}} \\
\end{align*}\\
$$

We can now swap to polar coordinates by using well-known identities.

$$
  \begin{align*}
    x &= r \cos(\theta) \\
    y &= r \sin(\theta) \\
    dx\, dy &= r dr\, d\theta\\
  \end{align*}
$$

Subbing everything in:

$$
  \begin{align*}
    \int\int{e^{-(x^2 + y^2)} dx\, dy} &= \int\int{e^{-(r \cos(\theta))^2 - (r \sin(\theta))^2} r dr\, d\theta } \\
    &= \int\int{e^{-r^2 (\cos(\theta)^2+\sin(\theta)^2 )} r dr\, d\theta} \\
    &= \int\int{e^{-r^2} r dr\, d\theta} \\
    &= \int_0^{2\pi} d\theta \int_0^{\infty} e^{-r^2} r dr \\
    &= 2\pi \int_0^{\infty} e^{-r^2} r dr \\
    &= 2\pi \int_0^{\infty} e^{-u} \frac{1}{2} du \\
    &= \pi\\
    \text{And so:}\\
   \int{e^{-x^2} dx} &= \sqrt{\pi}
\end{align*}
$$
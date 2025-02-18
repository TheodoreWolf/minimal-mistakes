---
layout: page
title: The score function trick for REINFORCE
importance: 2
category: derivations
---

The score function trick is just so elegant, the basis of many algorithms in ML. Here, I show it off for the REINFORCE policy gradient algorithm.

Consider a distribution of states $$d(s)$$ and a 
parameterised policy $$\pi_{\theta}(a | s)$$. The objective is to maximise the expected reward under the policy.

$$
\begin{align*}
  J(\theta) = \mathbb{E}_{\pi_\theta, d}[R(a, s)]\\
\end{align*}
$$

$$
\begin{align*}
  \nabla_{\theta} J(\theta) &= \nabla_{\theta} \int  d(s) ds  \int \pi_\theta(a | s) R(a, s) da \\
  &= \int d(s) ds \int \nabla_{\theta} \pi_\theta(a|s) R(a,s) da \\
  &= \int d(s) ds \int \pi_\theta(a|s) \frac{\nabla_{\theta} \pi_\theta(a|s)}{\pi_\theta(a|s)} R(a,s) da \\
\end{align*}
$$

We apply the score function trick: 
$$\nabla_{\theta} \log \pi_\theta(a|s) = \frac{\nabla_{\theta} \pi_\theta(a|s)}{\pi_\theta(a|s)}$$


$$
\begin{align*}
  \nabla_{\theta} J(\theta) &= \int d(s) ds \int \pi_\theta(a|s) \nabla_{\theta} \log \pi_\theta(a|s) R(a,s) da \\
  &= \mathbb{E}_{\pi_\theta, d}[\nabla_{\theta} \log \pi_\theta(a|s) R(a,s)] \\
\end{align*}
$$

We have moved the gradient operator inside the expectation. We can now estimate the gradient of the expected reward by sampling and therefore optimise our policy using gradient ascent.

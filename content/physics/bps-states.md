---
title: "BPS states and wall-crossing"
date: 2025-03-10
tags: ["string theory", "N=2", "BPS"]
math: true
summary: "Introduction to BPS states and the Kontsevich–Soibelman wall-crossing formula."
---

## What is a BPS state?

In supersymmetric theories a **BPS state** saturates the bound

$$M = |Z(\gamma)|$$

where $Z(\gamma)$ is the central charge evaluated on the charge vector
$\gamma \in \Gamma$. BPS states are annihilated by half the supercharges:

$$\bar{Q}_{\dot\alpha}|\text{BPS}\rangle = 0$$

## Wall-crossing

A wall of marginal stability $\mathcal{W}(\gamma_1,\gamma_2)$ is defined by

$$\operatorname{Im}\!\left(\frac{Z(\gamma_1)}{Z(\gamma_2)}\right) = 0$$

Crossing it, a state with charge $\gamma = \gamma_1 + \gamma_2$ can decay.
The **Kontsevich–Soibelman formula** tracks how BPS indices jump:

$$\prod_{\substack{\gamma\,\text{active} \\ \text{side A}}}
  \mathcal{K}_\gamma^{\Omega(\gamma)}
= \prod_{\substack{\gamma\,\text{active} \\ \text{side B}}}
  \mathcal{K}_\gamma^{\Omega(\gamma)}$$

## Code example
```python
import numpy as np

def central_charge(gamma, tau):
    """Compute Z(gamma) at modulus tau."""
    n, m = gamma
    return n + m * tau
```

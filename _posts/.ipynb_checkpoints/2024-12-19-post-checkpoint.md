---
title: 'Berry Phase'
date: 2024-12-19
permalink: /posts/2024-12-19-post
tags:
 
  - Quantum Mechanics 
  - Condensed Matter Physics


---


Topological Insulators and Topological Superconductors: Chapter 2
======

## General Formals

Consider a physical system with a general time-varying Hamiltonian $H(\textbf{R})$ that depends on time through several parameters labeled by a vector $\textbf{R}= (R1, R2, R3, . . . .)$ where $R_i = R_i (t)$.
$$
\begin{align}
H(\textbf{R})|n(\textbf{R})\rangle =E_n(\textbf{R})|n(\textbf{R})\rangle
\end{align}
$$
This equation determines the basis function $|n(\textbf{R})\rangle$ up to a phase, but we donot know the phase factor is what. Let the phase is $\theta(t)$ for state $|\Psi(t)\rangle=e^{-i\theta(t)}|n(\textbf{R})\rangle$. The time evolution of the system is given by 
$$
\begin{align}
H(\textbf{R(t)})|\Psi(t)\rangle =i \hbar \frac{d}{dt}|\Psi(t)\rangle
\end{align}
$$
Then translates into the differential equation 
$$
\begin{align}
E_n(\textbf{R}(t))|n(\textbf{R}(t))\rangle=\hbar (\frac{d}{dt}\theta(t))|n(\textbf{R}(t))\rangle+i \hbar \frac{d}{dt}|n(\textbf{R}(t))\rangle
\end{align}
$$
Taking the scalar product with $\langle n(\textbf{R}(t))|$ and assuming the state is normalized $\langle n(\textbf{R}(t))|n(\textbf{R}(t))\rangle$ = 1, we get 
$$
\begin{align}
E_n (\textbf{R}(t))-i \hbar\langle n(\textbf{R}(t))|\frac {d}{dt}| n(\textbf{R}(t))\rangle=\hbar(\frac{d}{dt} \theta(t))

\end{align}
$$
Then the solution for the phase $\theta (t)$ is
$$
\begin{align}
\theta(t)=\frac{1}{\hbar}\int_0^tE_n(\textbf{R}(t'))dt'-i\int_0^t\langle n(\textbf{R}(t'))|\frac{d}{dt'}|n(\textbf{R}(t'))\rangle dt'
\end{align}
$$
 The first part of  the phase is ==the conventional dynamical phase==. The negative of the second part is called ==the Berry phase==. If we write
$$
\begin{align}
|\Psi(t)\rangle=exp(\frac{1}{\hbar}\int_0^tE_n(\textbf{R}(t'))dt')\cdot exp(i \gamma_n)|n(\textbf{R}(t))\rangle
\end{align}
$$
With the Berry phase $\gamma_n$
$$
\begin{align}
\gamma_n=i\int_0^t\langle n(\textbf{R}(t'))|\frac{d}{dt'}|n(\textbf{R}(t'))\rangle dt'
\end{align}
$$
The Berry phase comes from the fact that the states at $t$ and $t + dt$ are not identical. Time can been removed explicitly from the equation, the only thing needed being the dependence of the eigenstates on the parameters $R_i$ , which are implicitly time dependent.
$$
\begin{align}
\gamma_n=i\int_0^{t_{end-cycle}}\langle n(\textbf{R}(t'))|\nabla_{\textbf{R}} |n(\textbf{R}(t'))\rangle \frac{d\textbf{R} }{dt'}dt'=i\int_C \langle n(\textbf{R}|\nabla_{\textbf{R}} |n(\textbf{R})\rangle d\textbf{R}
\end{align}
$$
By analogy with electron transport in an electromagnetic field, in the last equation we can now define a vector function called ==Berry connection==, or ==Berry vector potential==:
$$
\begin{align}
\textbf{A}_n(\textbf{R})=i \langle n(\textbf{R}|\frac{\partial}{\partial \textbf{R}} |n(\textbf{R})\rangle, \quad \gamma_n=\int_C d\textbf{R}\cdot \textbf{A}_n(\textbf{R})

\end{align}
$$
The Berry vector potential $A_n(\textbf{R})$ is gauge dependent. Under a gauge transformation $|n(\textbf{R})\rangle \rightarrow e^{i \zeta (\textbf{R})}|n(\textbf{R})\rangle$, with $\zeta (\textbf{R})$ a smooth, single-valued function, the Berry potential transforms in the usual way:
$$
\begin{align}
\textbf{A}_n(\textbf{R})\rightarrow \textbf{A}_n(\textbf{R})-\frac{\partial}{\partial \textbf{R} }\zeta (\textbf{R})
\end{align}
$$
As such, the Berry phase $\gamma _n$ will be changed by $-\int_C  \frac{\partial}{\partial \textbf{R} }\zeta (\textbf{R})\cdot d\textbf{R}=\zeta(\textbf{R}(0)-\textbf{R}(T))$ where $T$ is the long time after which the path $C$​ is completed. For a closed path, the Berry phase is a gauge- invariant quantity independent of the specific form of how $\textbf{R}$ varies in time. Because $C$ is a closed path, application of Stokes theorem gives:
$$
\begin{align}
\begin{gathered}\gamma_{n} =-\Im \int_{C} \langle n\left( \mathbf{R} \right) |\nabla_{\mathbf{R}} |n\left( \mathbf{R} \right) \rangle d\mathbf{R} =-\Im \int_{C} d\mathbf{S} \cdot \left( \nabla \times \langle n(\mathbf{R} \right) |\nabla |n\left( \mathbf{R} \right) \rangle )\\ =-\Im \int_{C} dS_{i}\varepsilon_{ijk} \nabla_{j} \langle n\left( \mathbf{R} \right) |\nabla_{k} |n\left( \mathbf{R} \right) \rangle =-\Im \int_{C} d\mathbf{S} \cdot \left( \langle \nabla n\left( \mathbf{R} \right) |\times|\nabla n\left( \mathbf{R} \right) \rangle \right)\end{gathered}\end{align}
$$
Where $ \langle \nabla n\left( \mathbf{R} \right) |\times|\nabla n\left( \mathbf{R} \right) \rangle $ is the ==Berry curvature==.

## Gauge-Independent Computation of the Berry Phase

At each $\textbf{R}$, we introduce a complete set of eigenstates $\sum_m|m\rangle\langle m|=1$
$$
\begin{align}
\begin{gathered}\varepsilon_{ijk} \langle \nabla_{j} n\left( \mathbf{R} \right) |\nabla_{k} |n\left( \mathbf{R} \right) \rangle\\ =\varepsilon_{ijk} \langle \nabla_{j} n\left( \mathbf{R} \right) |n\rangle \langle n|\nabla_{k} n\left( \mathbf{R} \right) \rangle +\sum_{m\neq n} \varepsilon_{ijk} \langle \nabla_{j} n\left( \mathbf{R} \right) |m\rangle \langle m|\nabla_{k} n\left( \mathbf{R} \right) \rangle\end{gathered}
\end{align}
$$
At first term, two parts are imaginary, so their product is real, then they have no contribution to the imaginary value that is used to compute the Berry phase. Hence, we get:
$$
\begin{align}
\gamma_{n} =-\Im \int_{S} dS_{i}\sum_{m\neq n} \varepsilon_{ijk} \langle \nabla_{j} n\left( \mathbf{R} \right) |m\rangle \langle m|\nabla_{k} n\left( \mathbf{R} \right) \rangle
\end{align}
$$
We massage this equation further to remove the derivatives on the eigenstates:
$$
\begin{align}
E_{n}\langle m|\nabla n\rangle =\langle m\nabla \left( Hn \right) \rangle =\langle m|\left( \nabla H \right) n\rangle +E_{m}\langle m|\nabla n\rangle
\end{align}
$$
Then we use $\langle m|n\rangle=\delta_{mn}$ , get:
$$
\begin{align}
\langle m|\nabla n\rangle =\frac{\langle m|\left( \nabla H \right) n\rangle }{E_n-E_m}
\end{align}
$$
Finally we could get a gauge independent experssion.
$$
\begin{align}
\begin{gathered}\gamma_{n} =-\int_{S} d\mathbf{S} \cdot \mathbf{V}_{n}\\ =-\int_{S} d\mathbf{S} \cdot \Im \sum_{m\neq n} \frac{\langle n\left( \mathbf{R} \right) |\left( \nabla_{\mathbf{R}} H\left( \mathbf{R} \right) \right) |m(\mathbf{R} )\rangle \times \langle m\left( \mathbf{R} \right) |(\nabla_{\mathbf{R}} H(\mathbf{R} ))|n\left( \mathbf{R} \right) \rangle}{\left( E_{m}\left( \mathbf{R} \right) -E_{n}\left( \mathbf{R} \right) \right)^{2}}\end{gathered}
\end{align}
$$
This equation shows that the Berry curvature can be thought of as the result of the interaction with the level $|n\rangle$ of the other levels $ |m\rangle $ that have been projected out by the adiabatic interaction. 

## Degeneracies and Level Crossing

One of the most important applications of the Berry phase is the classification of degeneracies. 

Consider two states $\pm$, of energies $E_-(\textbf{R}) \leqslant E_+(\textbf{R})$ with a degeneracy $E_-(\textbf{R}^*) = E_+(\textbf{R}^*)$. For $\textbf{R}$ close to the degeneracy point $\textbf{R}^*$, the Hamiltonian can be expanded in $\textbf{R}-\textbf{R}^*$ as $H(\textbf{R})=H(\textbf{R}^*)+(\textbf{R}-\textbf{R}^*)\cdot \nabla H(\textbf{R}^*)$, thereby giving the following for the Berry curvature:
$$
\begin{align}
\mathbf{V}_{+} (\mathbf{R} )=\Im \frac{\langle +\left( \mathbf{R} \right) |\left( \nabla H\left( \mathbf{R}^{\ast} \right) \right) |-\left( \mathbf{R} \right) \rangle \times \langle -\left( \mathbf{R} \right) |\left( \nabla H\left( \mathbf{R}^{\ast} \right) \right) |+\left( \mathbf{R} \right) \rangle}{\left( E_{+}\left( \mathbf{R} \right) -E_{-}\left( \mathbf{R} \right) \right)^{2}}
\end{align}
$$
 Because of the cross product, $\mathbf{V}_{-} \left( \mathbf{R} \right) =-\mathbf{V}_{+} \left( \mathbf{R} \right)$, and hence $\gamma_{-} \left( C \right) =-\gamma_{+} \left( C \right)$.

The generic form of the Hamiltonian of any two level system is:
$$
\begin{align}
H=\varepsilon \left( \mathbf{R} \right) I_{2\times 2}+\mathbf{d} \left( \mathbf{R} \right) \cdot \sigma
\end{align}
$$
Where $\sigma^i$ are the Pauli matrices and $\textbf{d}$ is a 3-D vector that depends on the coordinates $\textbf{R}$. 




















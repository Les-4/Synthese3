---
layout: default
title: Transforme de fourier
parent: TDS
---

<!-- transforme_fourier.html -->
  <head>
    <meta charset="utf-8">
    <script type="text/x-mathjax-config">
        MathJax.Hub.Config({
        tex2jax: {inlineMath: [['$','$'], ['\\(','\\)']]}
        });
    </script>
   <script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
    <script type="text/javascript" async src="{{site.cdnjs}}"></script>
    <script type="text/javascript" async src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.7/MathJax.js?config=TeX-MML-AM_CHTML"></script>
    <!-- <script async src="https://cdn.jsdelivr.net/npm/mathjax@2/MathJax.js?config=TeX-AMS-MML_CHTML"></script> -->
    <!-- <script async src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.1/MathJax.js?config=TeX-AMS-MML_HTMLorMML"></script> -->
  </head>

## Transformé de fourier

**Rappel**

Soit un signal $s(t)$

-   la valeur moyenne $a_0$ du signal est est defini par la formule

$a_0 = \frac{1}{t} \times \displaystyle \int_{- \frac{t}{2}}^{\frac{t}{2}} s(t) \, \mathrm{dt}$

-   Pour le calcul des coefficients $a_n$

$a_n = \frac{2}{t} \times \displaystyle \int_{- \frac{t}{2}}^{\frac{t}{2}} s(t) \times \cos(2\pi nF_0t)\, \mathrm{dt}$

-   Pour le calcul des coefficients $b_n$

$b_n = \frac{2}{t} \times \displaystyle \int_{- \frac{t}{2}}^{\frac{t}{2}} s(t) \times \sin(2 \pi nF_0t)\, \mathrm {dt}$

Soit le schema suivant en dent de scie :

Il nous est demandé de trouver l'équation de et les 3 premiers termes de la
transformé de fourier

On peut deduire l'équation de ce schéma:

$s(t)= \left\{\begin{array}{ll} \ 0 \ \forall \ t \ \in \left[-\pi , 0 \right] \\ \ t \ \forall \  t \in \left[ 0 , \pi\right]\end{array} 
\right.$

On donne la fréquence fondamentale : F = $\frac{1}{2\pi}$ $\Rightarrow
\frac{1}{t} = \frac{1}{2 \pi} $

1. Trouvons la valeur moyenne de notre signal :

En général on a :

$a_0 = \frac{1}{2 \pi} \left(\displaystyle \int_{-\pi}^{0} s(t).\cos(nt)\mathrm{dt} + \displaystyle \int_{0}^{\pi} s(t).\cos(nt) \mathrm{dt} \right)$

$=  \frac{1}{2 \pi} \left(\displaystyle \int_{-\pi}^{0} 0.\cos(0.t)\mathrm{dt} + \displaystyle \int_{0}^{\pi} t.\cos(0.t) \mathrm{dt} \right)$

$= \frac{1}{2 \pi} \left(\displaystyle \int_{-\pi}^{0} 0 \mathrm{dt} + \displaystyle \int_{0}^{\pi} t\mathrm{dt} \right)$

$= \frac{1}{2\pi} \left(0+ \left[ \frac{t^2}{2} \right]_0^\pi \right)$

$= \frac{1}{2\pi}\left( \frac{\pi^2}{2}\right)$

$=\frac{\pi}{4}$

2. Trouvons les premier terme de $a_n$

puisque $F= \frac{1}{2\pi} \Rightarrow \frac{2}{t}=\frac{1}{\pi}$

$a_n = \frac{1}{\pi} \left(\displaystyle \int_{-\pi}^{0} s(t).\cos(nt)\mathrm{dt} + \displaystyle \int_{0}^{\pi} s(t).\cos(nt) \mathrm{dt} \right)$

$= \frac{1}{\pi} \left(\displaystyle \int_{-\pi}^{0} 0.\cos(nt)\mathrm{dt} + \displaystyle \int_{0}^{\pi} t.\cos(nt) \mathrm{dt} \right)$

$= \frac{1}{\pi} \left( \displaystyle \int_{0}^{\pi} t.\cos(nt) \mathrm{dt} \right)$

On peut appliquer la méthode d'intégration par partie à cette fontin :

**Rappel integration par partie**

soit l'intégrale suivante:

$\displaystyle \int_{}^{} f.g'$

$= \left[ f.g \right] - \displaystyle \int_{}^{} f'g \ \mathrm{dt}$

Dans notre cas, considérons

$f = t \ \ \Rightarrow \ \ f' = 1$

$g' = \cos(nt) \ \ \Rightarrow \ \ g =
\frac{\sin(nt)}{n}$

$ \Rightarrow \displaystyle \int*{0}^{\pi} t.\cos(nt) \mathrm{dt} = \left[t
\times \frac{\sin(nt)}{n} \right]\*{0}^{\pi} - \displaystyle \int*{0}^{\pi} 1
\times\frac{\sin(nt)}{n} \mathrm{dt}$

$= \pi \times \frac{\sin(n.\pi)}{n} - 0 \times \frac{\sin(n.0)}{n} - \left[ \frac{\cos(nt)}{n^2}\right]_{0}^{\pi}$

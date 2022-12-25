## Dilatation

Soit un élément structurant (1,1,1)

Soit la matrice suivante

$$
\left(\begin{array}{cc}
1&1&0&0&1&0&1\\
1&1&0&1&1&0&1\\
0&1&0&0&0&0&1\\
0&0&0&0&0&1&1\\
1&1&0&0&0&0&0\\
1&0&0&0&0&0&0\\
\end{array}\right)
$$

Pour faire une dilation vous devez prendre l'élément centrale de l'élément
structurant (1,**1**,1) et le positionner sur chaque point de la matrice. si
lorsque tu as positionner ton élément structurant sur ta matrice tous les
éléments de ta matrice sont à 0 alors le point de la matrice qui est sur le
point centrale de ton élément structurant devient 0 par contre s'il y'a au moins
un 1 alors le point devient 1

_Dans notre matrice précédente, prenons l'avant derniere ligne et déplaçons
l'élément structurant dessus_

L'avant dernière ligne est : (1 1 0 0 0 0 0)

-   Placons le point centrale de l'élément structurant sur le premier point de
    la ligne :

$$
\left(\begin{array}{cc}
*1*&1\\
1&1&0&0&0&0&0\\
\end{array}\right)
$$

comme on à au moins 1 sur la ligne le premier point reste 1

-   Placons le point centrale de l'élément structurant Pour le deuxieme point de
    la ligne on aura
    $$
    \left(\begin{array}{cc}
    1&*1*&1\\
    1&1&0&0&0&0&0\\
    \end{array}\right)
    $$

Comme on a (1 1 0) on a un élément qui est à 1 donc le second point devient 1 et
la ligne devient

$$
\left(\begin{array}{cc}
1&1&0&0&0&0&0\\
\end{array}\right)
$$

-   Pour le troisième point de la ligne on aura
    $$
    \left(\begin{array}{cc}
    &1&*1*&1\\
    1&1&0&0&0&0&0\\
    \end{array}\right)
    $$

Comme on a (1 0 0) on a un élément à 1 donc le troisième point devient 1 et la
ligne devient

$$
\left(\begin{array}{cc}
1&1&1&0&0&0&0\\
\end{array}\right)
$$

-   Pour le quatrième point de la ligne on aura
    $$
    \left(\begin{array}{cc}
    &&1&*1*&1\\
    1&1&0&0&0&0&0\\
    \end{array}\right)
    $$

comme on a (0 0 0) on a aucun élément à 1 donc le quatrième point de la ligne
restera à 0 et ainsi de suite la ligne sera

$$
\left(\begin{array}{cc}
1&1&1&0&0&0&0\\
\end{array}\right)
$$

Notre matrice finale sera donc

$$
\left(\begin{array}{cc}
1&1&1&1&1&1&1\\
1&1&1&1&1&1&1\\
1&1&1&0&0&1&1\\
0&0&0&0&1&1&1\\
1&1&1&0&0&0&0\\
1&1&0&0&0&0&0\\
\end{array}\right)
$$


## Erosion

Reprenons notre exemple précédent, au lieu de remplacer par des 1 lorsqu'on 1, on remplace par 0 lorsqu'on à au moins un 0 superposé à notre élément structurant sur la ligne

**Ex** : Notre avant dernière ligne sera :

- pour le premier point
$$
\left(\begin{array}{cc}
*1*&1\\
1&1&0&0&0&0&0\\
\end{array}\right)
$$

- pour le second point

$$
\left(\begin{array}{cc}
1&*1*&1\\
1&1&0&0&0&0&0\\
\end{array}\right)
$$

La ligne devient :
$$
\left(\begin{array}{cc}
1&0&0&0&0&0&0\\
\end{array}\right)
$$

- pour le troisième point
$$
\left(\begin{array}{cc}
&1&*1*&1\\
1&1&0&0&0&0&0\\
\end{array}\right)
$$

la ligne devient
$$
\left(\begin{array}{cc}
1&0&0&0&0&0&0\\
\end{array}\right)
$$

Et ainsi de suite on aura notre matrice finale qui sera 

$$
\left(\begin{array}{cc}
1&0&0&0&0&0&0\\
1&0&0&0&0&0&0\\
0&0&0&0&0&0&0\\
0&0&0&0&0&0&1\\
1&0&0&0&0&0&0\\
0&0&0&0&0&0&0\\
\end{array}\right)
$$
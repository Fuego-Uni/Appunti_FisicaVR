# Componenti

Un vettore ha 3 componenti:
- Modulo (la lunghezza del vettore)
- Direzione
- Verso

![[intro/intro_images.md#^group=9mwb65ymMaGDmzlcbsplg]]

#versore : vettore di modulo 1, $\hat{v}$

ogni vettore è scomponibile in una somma di versori cartesiani (versori paralleli agli assi, generalmente $\hat{i}$ e $\hat{j}$):

$\hat{a} = a_x\hat{i}\ +\ a_y\hat{j}\ = (a_x, a_j)$


# Operazioni

- **Interna**: produce un vettore come risultato ^opint
- **esterna**: produce uno scalare come risultato ^opest

## Somma vettoriale
$\vec{a} + \vec{b} = (a_x+b_x)\hat{i} + (a_y+b_y)\hat{j} = (a_x+b_x, a_y+b_y)$ 

Operazione [[Vettori#^opint|Interna]]

![[intro/intro_images.md#^group=uhPpC0A0lUu5zXsVIGkGx]]


## Prodotto scalare (dot product)
$\vec{a} \cdot \vec{b} = (a_xb_x)+(a_yb_y)$

Operazione [[Vettori#^opest|esterna]]

Restituisce un valore che rappresenta quanto sono "paralleli" due vettori, il valore:
- tende a 0 se l'angolo fra i vettori tende a 90 deg
- è >0 se l'angolo è < 90 deg (vettori con **versi** simili)
- è <0 se l'angolo è > 90 deg (vettori con **versi** opposti)

$\vec{a} \cdot \vec{b} = ab \cos(\theta) = ab_a$
(*$b_a$ è la proiezione di b su a*)
![[intro/intro_images.md#^group=dj7B0MNq4V5fPlHKKeNcK]]

#### casi particolari:

- $\vec{a} \parallel \vec{b} \Rightarrow \vec{a} \cdot \vec{b} = ab$
![[intro/intro_images.md#^group=iLZtxWdC]]


- $\vec{a} \perp \vec{b} \Rightarrow \vec{a} \cdot \vec{b} = 0$
![[intro/intro_images.md#^group=jgHjV6Rt]]

## Prodotto vettoriale

Operazione [[Vettori#^opint|Interna]]

Per calcolare le componenti del vettore risultante:

- **Direzione**: è perpendicolare ai vettori moltiplicati
![[intro/intro_images.md#^group=JVevsOfvQkfpbhjsCRVFo]]

- **Verso**: regola della mano destra, l'ordine dei moltiplicandi è importante: $\hat{a} \times \hat{b} = -(\hat{b} \times \hat{a})$
![[intro/intro_images.md#^group=1cmhBxBEQfxdGvXykASWo]]

- **Modulo**: $ab\sin(a)$

#### casi particolari:
$\vec{a} \parallel \vec{b} \Rightarrow \vec{a} \wedge \vec{b} = 0$
$\vec{a} \perp \vec{b} \Rightarrow \vec{a} \cdot \vec{b} = ab$

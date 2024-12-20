- [Introduzione](#introduzione)
  - [Prodotto scalare Euclideo](#prodotto-scalare-euclideo)
  - [Parallelismo](#parallelismo)
  - [Ortogonalità](#ortogonalità)
  - [Equazioni lineari](#equazioni-lineari)
  - [Sistemi lineari](#sistemi-lineari)
  - [Struttura algebrica di $\\mathbb{R}^n$](#struttura-algebrica-di-mathbbrn)
    - [Somma](#somma)
  - [Prodotto per scalare](#prodotto-per-scalare)

# Introduzione

**Sottospazio affine** = Lo spazio delle soluzioni di un sistema di equazioni lineari.

Piano = **luogo di zeri** dell'applicazione lineare.

Un’applicazione lineare può essere rappresentata da una matrice.

Operazioni naturali sullo spazio delle applicazioni lineari si riflettono in operazioni sulle matrici.

Alcune proprietà delle applicazioni lineari si riflettono in proprietà delle matrici.

## Prodotto scalare Euclideo

$$((x_1, y_1), (x_2, y_2))\rightarrow x_1x_2+y_1y_2$$

## Parallelismo

Date due rette $y=mx+q$ e $y=m'x+p'$:

$$m=m'\Rightarrow \text{Le due rette sono parallele.}$$

## Ortogonalità

Date due rette passanti per O e i rispettivi punti $(a, b)$ e $(a', b')$

$$aa'+bb'=0\Rightarrow\text{Le due rette sono ortogonali.}$$

## Equazioni lineari

Un’equazione lineare nelle incognite $x_1 , . . . , x_k$ a coefficienti reali è
un’equazione della forma:

$$a_1x_1 + . . . + a_kx_k=b$$

L’insieme delle soluzioni dell'equazione è:

$$\lbrace(x_1 , . . . , x_n)\in\mathbb{R}^n|a_1x_1+...+a_nx_n=b\rbrace$$

$$b=0\Leftrightarrow \text{Equazione omogenea}$$

$$\text{Equazioni equivalenti} \Leftrightarrow \text{Stesse soluzioni}$$

## Sistemi lineari

Un sistema di equazioni lineari $x_1 , . . . , x_n$ a coefficienti reali è un
insieme di equazioni lineari nelle incognite $x_1 , . . . , x_n$ a coefficienti in
$\mathbb{R}$:

$$
\begin{cases}
    a_{11}x_1+...+a_{1n}x_n=b_1\\
    \vdots\\
    a_{m1}x_1+...+a_{mn}x_n=b_m\\
\end{cases}
$$

Dato un sistema lineare, l'insieme delle soluzioni è:

$$
\left\lbrace
(x_1 , . . . , x_n)\in\mathbb{R}^n\ \big|
\begin{cases}
    a_{11}x_1+...+a_{1n}x_n=b_1\\
    \vdots\\
    a_{m1}x_1+...+a_{mn}x_n=b_m\\
\end{cases}
\right\rbrace
$$

Un sistema è omogeneo se ogni sua componente è omogenea:

$$\text{Sistema omogeneo}\Leftrightarrow \forall i\in[1:m]\mid b_i = 0$$

$$\text{Sistemi equivalenti} \Leftrightarrow \text{Stesse soluzioni}$$

## Struttura algebrica di $\mathbb{R}^n$

Su $\mathbb{R}^n$ esistono due operazioni naturali:

### Somma

$$\mathbb{R}^n\times\mathbb{R}^n\rightarrow\mathbb{R}^n$$
$$(x_1,...,x_n)+(y_1,...,y_n)=(x_1y_1,...,x_ny_n)$$

## Prodotto per scalare

$$\mathbb{R}\times\mathbb{R}^n\rightarrow\mathbb{R}^n$$

$$\lambda(x_1,...,x_n)=(\lambda x_1,...,\lambda x_n)$$

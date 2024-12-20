- [Introduzione](#introduzione)
  - [Prodotto scalare Euclideo](#prodotto-scalare-euclideo)
  - [Parallelismo](#parallelismo)
  - [Ortogonalità](#ortogonalità)
  - [Equazioni lineari](#equazioni-lineari)
  - [Sistemi lineari](#sistemi-lineari)
  - [Struttura algebrica di $\\mathbb{R}^n$](#struttura-algebrica-di-mathbbrn)
    - [Terminologia](#terminologia)
    - [Proprietà](#proprietà)
  - [matrici](#matrici)
  - [Operazioni con le matrici](#operazioni-con-le-matrici)
    - [Somma](#somma)
    - [Prodotto matrice per scalare](#prodotto-matrice-per-scalare)
    - [Matrice incompleta, completa](#matrice-incompleta-completa)
  - [Sistemi e matrici a scala](#sistemi-e-matrici-a-scala)
  - [Proposizione](#proposizione)
- [Eliminazione di Gauss](#eliminazione-di-gauss)
  - [Proposizione](#proposizione-1)
  - [Metodo di eliminazione di Gauss](#metodo-di-eliminazione-di-gauss)
  - [Esempio](#esempio)
- [Prodotto matrice per vettore](#prodotto-matrice-per-vettore)
  - [Proprietà](#proprietà)
  - [Proposizione](#proposizione-2)
- [Spazi e sottospazi](#spazi-e-sottospazi)
  - [Spazio vettiriale](#spazio-vettiriale)
  - [Sottospazio vettiriale](#sottospazio-vettiriale)
- [Spazio dei polinomi](#spazio-dei-polinomi)

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

Un’equazione lineare nelle incognite $x_1 ,\dots, x_k$ a coefficienti reali è
un’equazione della forma:

$$a_1x_1 +\cdots+ a_kx_k=b$$

L’insieme delle soluzioni dell'equazione è:

$$\lbrace(x_1 ,\dots, x_n)\in\mathbb{R}^n|a_1x_1+\cdots+a_nx_n=b\rbrace$$

$$b=0\Leftrightarrow \text{Equazione omogenea}$$

$$\text{Equazioni equivalenti} \Leftrightarrow \text{Stesse soluzioni}$$

## Sistemi lineari

Un sistema di equazioni lineari $x_1 ,\dots, x_n$ a coefficienti reali è un
insieme di equazioni lineari nelle incognite $x_1 ,\dots, x_n$ a coefficienti in
$\mathbb{R}$:

$$
\begin{cases}
    a_{11}x_1+\cdots+a_{1n}x_n=b_1\\
    \vdots\\
    a_{m1}x_1+\cdots+a_{mn}x_n=b_m\\
\end{cases}
$$

Dato un sistema lineare, l'insieme delle soluzioni è:

$$
\left\lbrace
(x_1 ,\dots, x_n)\in\mathbb{R}^n\ \big|
\begin{cases}
    a_{11}x_1+\cdots+a_{1n}x_n=b_1\\
    \vdots\\
    a_{m1}x_1+\cdots+a_{mn}x_n=b_m\\
\end{cases}
\right\rbrace
$$

Un sistema è omogeneo se ogni sua componente è omogenea:

$$\text{Sistema omogeneo}\Leftrightarrow \forall i\in[1:m]\mid b_i = 0$$

$$\text{Sistemi equivalenti} \Leftrightarrow \text{Stesse soluzioni}$$

## Struttura algebrica di $\mathbb{R}^n$

Su $\mathbb{R}^n$ esistono due operazioni naturali:

- ### Somma

$$\mathbb{R}^n\times\mathbb{R}^n\rightarrow\mathbb{R}^n$$
$$(x_1,\dots,x_n)+(y_1,\dots,y_n)=(x_1y_1,\dots,x_ny_n)$$

- ### Prodotto per scalare

$$\mathbb{R}\times\mathbb{R}^n\rightarrow\mathbb{R}^n$$

$$\lambda(x_1,\dots,x_n)=(\lambda x_1,\dots,\lambda x_n)$$

Dato un sistema lineare:

$$
\begin{cases}
    a_{11}x_1+\cdots+a_{1n}x_n=b_1\\
    \vdots\\
    a_{m1}x_1+\cdots+a_{mn}x_n=b_m\\
\end{cases}\\
\space\\
(x_1 , \dots, x_n)\in\mathbb{R}^n=soluzione\\
\Leftrightarrow\\
x_1
    \begin{pmatrix}
        a_{11}\\
        \vdots\\
        a_{m1}
    \end{pmatrix}
+ \cdots + x_n
    \begin{pmatrix}
        a_{1n}\\
        \vdots\\
        a_{mn}
    \end{pmatrix}
=
    \begin{pmatrix}
        b_1\\
        \vdots\\
        b_m
    \end{pmatrix}
$$

### Terminologia

Elemento $\mathbb{R}^n$ = vettore

Elemento $\mathbb{R}$ = scalare

### Proprietà

1. $(v + w) + u = v + (w + u)$
2. $v + \mathbf{0} = v = \mathbf{0} + v$
3. $v + (-1)v = \mathbf{0} = (-1)v + v$
4. $v + w = w + v$
5. $\lambda(\mu v) = (\lambda \mu)v$
6. $\lambda(v + w) = (\lambda v) + (\lambda w)$
7. $(\lambda + \mu)v = \lambda v + \mu v$
8. $1v = v$

$$\forall\space\lambda\mu\in\mathbb{R}\land u, v, w\in\mathbb{R}^n$$

## matrici

Una matrice $m\times n$ a coefficienti in $\mathbb{R}$ = tabella con $m$ righe ed $n$ colonne di elementi di $\mathbb{R}$:

$$
A=\begin{pmatrix}
    a_{11}&\cdots&a_{1n}\\
    \vdots&&\vdots\\
    a_{m1}&\cdots&a_{mn}
\end{pmatrix}
$$

Un vettore riga è una matrice $1\times n$; un vettore colonna è una
matrice $m\times1$.

La riga i-esima della matrice $(a_{ij})$ è il vettore:

$$A_i=(a_{i1},\dots,a_{in});$$

La colonna j-esima della matrice $(a_{ij})$ è il vettore:

$$
A^j=\begin{pmatrix}
    a_{1j}\\
    \vdots\\
    a_{mj}
\end{pmatrix}
$$

Fissati $m$ ed $n$, l’insieme delle matrici $m\times n$ a coefficienti in $\mathbb{R}$ si indica
con $M_{m,n} (\mathbb{R})$.

Vettori riga e colonna si identificano con le n-uple. Le matrici $1\times 1$ si
identificano con gli scalari.

## Operazioni con le matrici

### Somma

Date due matrici $m\times n$:

$$A=(a_{ij}), B=(b_{ij})$$

La matrice $m\times n$:

$$C=(c_{ij})\ |\ c_{ij} = a_{ij}+b_{ij}$$

è detta somma di $A$ e $B$ e si scrive $C=A+B$.

### Prodotto matrice per scalare

Date una matrice $m\times n$:

$$A=(a_{ij})$$

ed uno scalare $\lambda\in\mathbb{R}$, la matrice $m\times n$:

$$B=(b_{ij}), b_{ij}=\lambda a_{ij}$$

è detta prodotto di $A$ per $\lambda$ e si scrive $B=\lambda A$

### Matrice incompleta, completa

Dato un sistema lineare:

$$
\begin{cases}
    a_{11}x_1+\cdots+a_{1n}x_n=b_1\\
    \vdots\\
    a_{m1}x_1+\cdots+a_{mn}x_n=b_m\\
\end{cases}\\
$$

Matrice dei coefficienti o incompleta:

$$
A=(a_{ij}) =\begin{pmatrix}
    a_{11}&\cdots&a_{1n}\\
    \vdots&&\vdots\\
    a_{m1}&\cdots&a_{mn}
\end{pmatrix}
$$

Matrice completa

$$
(A|B) = \left(\begin{array}{ccc|c}
a_{11} & \cdots & a_{1n} & b_1 \\
\vdots & \ddots & \vdots & \vdots \\
a_{m1} & \cdots & a_{mn} & b_m
\end{array}\right)
$$

## Sistemi e matrici a scala

Data una matrice $A$, se $A_i$ è una riga di elementi non tutti nulli, diciamo
che il pivot sulla riga $A_i$ è il primo elemento non nullo.

La matrice si dice a scala se valgono le seguenti condizioni:

- ogni pivot è strettamente a destra dei pivot delle righe precedenti;
- Le righe senza pivot stanno sotto le righe con un pivot.

Un sistema lineare è a scala se la matrice incompleta è a scala.

$$
\begin{pmatrix}
a_{11} & \cdots & \cdots & \cdots & a_{1n} \\
0 & a_{22} & \cdots & \cdots & a_{2n} \\
0 & 0 & \ddots & & \vdots \\
0 & 0 & 0 & a_{rr} & \cdots & a_{rn} \\
0 & 0 & 0 & 0 & \cdots & 0 \\
\vdots & \vdots & \vdots & \vdots & \ddots & \vdots \\
0 & 0 & 0 & 0 & \cdots & 0
\end{pmatrix}
$$

## Proposizione

Dato un sistema lineare a coefficienti in $\mathbb{R}$ di $m$ equazioni in $n$ incognite
la cui matrice incompleta è a scala con $r$ pivot:

- $\exists i\in[r+1,m]\ |\ b_i\neq 0\Rightarrow$ non esiste soluzione;
- $\forall i\in[r+1,m]\ |\ b_i=0\Rightarrow$ esiste una soluzione:
  - $r=n\Rightarrow$ la soluzione è unica;
  - $r<n\Rightarrow$ le soluzioni sono in corrispondenza biunivoca con $\mathbb{R}^{n-r}$.

# Eliminazione di Gauss

## Proposizione

Applicando a un sistema lineare una delle seguenti operazioni:

1. moltiplicare un'equazione per uno scalare diverso da 0;
2. scambiare due equazioni;
3. aggiungere a un'equazione un multiplo di un'altra,

si ottiene un sistema lineare equivalente.

## Metodo di eliminazione di Gauss

Consiste nel trasformare un sistema lineare con matrice completa $(A|B)$
in un sistema a scala applicando operazioni elementari.

1. Se $A$ è la matrice nulla, è già a scala.
2. Altrimenti, identificare la prima colonna non nulla $A^k$ di $A$.
3. Tra gli elementi di $A^k$ uno è non nullo. Sceglierne uno, diciamo $a_{hk}$ ;
   se $h\neq1$, scambiare la riga h-esima della matrice completa con la
   prima.
4. $\forall\ i > 1$, sommare alla riga i-esima un multiplo della prima
   riga in modo che il termine $a_{ik}$ diventi zero.
5. Ripetere il processo per la sottomatrice.

## Esempio

$$
\begin{cases}
2x_1 + x_2 + 3x_3 &= 2 \\
x_1 - x_2 &= 3 \\
2x_1 + 2x_3 &= 1 \\
-x_1 + x_2 &= 3
\end{cases}
$$

$$
\left(\begin{array}{ccc|c}
2 & 1 & 3 & 2\\1 & -1 & 0 & 3\\2 & 0 & 2 & 1\\-1 & 1 & 0 & 3
\end{array}
\right)\begin{array}{c}
I + 2\cdot IV\\II + IV\\III + 2\cdot IV\\I\leftrightarrow IV\\
\end{array}\rightarrow

\left(\begin{array}{ccc|c}
-1 & 1 & 0 & 3\\0 & 0 & 0 & 6\\0 & 2 & 2 & 7 \\0 & 3 & 3 & 8
\end{array}
\right)\\\ \\
b_2\neq0\Rightarrow\text{Il sistema non ha soluzione}
$$

# Prodotto matrice per vettore

Data una matrice $m\times n$:

$$A = (a_{ij})$$

ed un vettore colonna:

$$
B=\begin{pmatrix}
    b_1\\
    \vdots\\
    b_n
\end{pmatrix}
$$

il prodotto $AB$ è definito come il vettore:

$$AB=b_1A_1+\cdots+b_nA_n$$

(colonna per riga)

Introdotto il vettore delle incognite:

$$
X=\begin{pmatrix}
    x_1\\
    \vdots\\
    x_n
\end{pmatrix}
$$

un sistema lineare con matrice completa (A|B) può essere scritto nella forma:

$$AX=B$$

## Proprietà

Siano $A$, $B$ matrici $m\times n$ e siano $X$, $Y$ vettori con $n$ componenti; sia $\lambda$
uno scalare, vale che:

1. $A(X+Y)=AX+AY$;
2. $(A+B)X=AX+AB$;
3. $A(\lambda X)=\lambda(AX)$.

## Proposizione

Data $A\in M_{m,n} (\mathbb{R})$, sia $W$ l'insieme delle soluzioni del sistema lineare
omogeneo $AX = 0$. Dato $B\in R_n$, se il sistema lineare $AX = B$ ammette
una soluzione $X_0$, le sue soluzioni sono tutte e soli i vettori:

$$X_0 + Y\in\mathbb{R}^n,$$

al variare di $Y\in W$.

# Spazi e sottospazi

## Spazio vettiriale

Uno spazio vettoriale reale è un insieme V su cui sono definite due
operazioni:

$$V\times V\rightarrow V,\quad(v,w)\rightarrow v+w$$

$$\mathbb{R}\times V\rightarrow V,\quad(a,v)\rightarrow av$$

che soddisfano le seguenti proprietà:

- $(v+w)+u=v+(w+u)$;
- $\exist 0\in V | V+0=V=0+V$;
- $v+(-1)v=0=(-1)v+v$;
- $v+w=w+v$;
- $\lambda(\mu v)=(\lambda\mu)v$;
- $\lambda(v+w)=(\lambda v)+(\lambda w)$;
- $(\lambda+\mu)v=\lambda v+\mu v$;
- $1v=v$;
- Elemento $V$ = vettore;
- Elemento $\mathbb{R}$ = scalare.

## Sottospazio vettiriale

Dato uno spazio vettoriale V, un sottospazio di V è $W\subset V\ |$ :

- $0\in W$
- $v,w\in W\Rightarrow v+w\in W$
- $v\in W\land c\in\mathbb{R}\Rightarrow cv\in W$

Il sottospazio $W\subset V$ è ancora uno spazio vettoriale.

# Spazio dei polinomi

Sia $a:N\rightarrow R$ una funzione:
$$(i\rightarrow a_i | \exist n\in\mathbb{N}\ |\ \forall i\in[0, n]\ .\ a_i\neq 0)$$

Polinomio a coefficienti reali nell'indeterminata $x$:

$$p=a_0x^0+\cdots a_nx^n$$

Per costruzione, 0 è un polinomio ($\forall i\in[0, n]\ .\ a_i=0$);

Il grado di $p\neq0$ viene indicato con $deg\ p$ ed è uguale a $n$, $deg\ 0 =-\infty$;

L'insieme dei polinomi a coefficienti reali nell'indeterminata $x$ si
indica con $\mathbb{R}[x]$.

Lo spazio dei polinomi ha una struttura di spazio vettoriale.

# Gaussian Integers, Powers of Two, and Sums of Two Squares

**Author:** Shaimaa Said Soltan

This note describes how ordinary integers can be studied using Gaussian integers

$$
\mathbb Z[i]=\{a+bi:a,b\in\mathbb Z\},
$$

and explains the different behavior of odd numbers congruent to $1$ and $3$ modulo $4$.

## 1. Powers of $1+i$

The number $1+i$ has magnitude $\sqrt 2$ and argument $\pi/4$:

$$
1+i=\sqrt2\left(\cos\frac{\pi}{4}+i\sin\frac{\pi}{4}\right).
$$

Therefore,

$$
(1+i)^x=2^{x/2}
\left(\cos\frac{x\pi}{4}+i\sin\frac{x\pi}{4}\right).
$$

### Even and odd exponents

For an integer exponent $x\geq0$, the direction of $(1+i)^x$ repeats every eight powers. This gives the piecewise representation

$$
\boxed{
(1+i)^x=
\begin{cases}
2^{x/2}(a+bi),
&x\text{ even},\quad |a|+|b|=1,\\[4pt]
2^{(x-1)/2}(a+bi),
&x\text{ odd},\quad |a|=|b|=1,
\end{cases}}
$$

where $a,b\in\{-1,0,1\}$. The factor $a+bi$ is determined by $x$; it is not arbitrary. More precisely,

$$
a+bi=
\begin{cases}
i^{x/2},&x\text{ even},\\[4pt]
i^{(x-1)/2}(1+i),&x\text{ odd}.
\end{cases}
$$

Dividing out this direction factor leaves a nonnegative power of two:

$$
\boxed{
\frac{(1+i)^x}{a+bi}=
\begin{cases}
2^{x/2},&x\text{ even},\\[4pt]
2^{(x-1)/2},&x\text{ odd}.
\end{cases}}
$$

Equivalently,

$$
\boxed{
\frac{(1+i)^x}{a+bi}=2^{\lfloor x/2\rfloor}.
}
$$

Consequently, every nonnegative power $2^n$ has two consecutive-exponent representations:

$$
\boxed{2^n=\frac{(1+i)^{2n}}{i^n}}
$$

and

$$
\boxed{2^n=\frac{(1+i)^{2n+1}}{i^n(1+i)}}.
$$

The even exponent reaches one of the coordinate axes, while the following odd exponent lies on a diagonal. Dividing by the corresponding direction factor returns the same positive real number $2^n$.

For every nonnegative integer $e$,

$$
(1+i)^{2e}=2^e i^e,
$$

so every power of two can be written as

$$
\boxed{2^e=\frac{(1+i)^{2e}}{i^e}}.
$$

Multiplication by $1+i$ rotates a point by $45^\circ$ and multiplies its magnitude by $\sqrt2$. Division by $1+i$ rotates it by $-45^\circ$ and divides its magnitude by $\sqrt2$.

Because

$$
2=-i(1+i)^2,
$$

each ordinary factor of $2$ corresponds to two factors of $1+i$ in $\mathbb Z[i]$.

If

$$
N=2^e m,\qquad m\text{ odd},
$$

then the maximum number of factors $1+i$ that can be extracted from $N$ is $2e$.

## 2. Every odd integer is a difference of two squares

For an odd positive integer $m$, define

$$
A=\frac{m+1}{2},\qquad B=\frac{m-1}{2}.
$$

Then

$$
A^2-B^2=(A+B)(A-B)=m.
$$

Thus,

$$
\boxed{
m=
\left(\frac{m+1}{2}\right)^2-
\left(\frac{m-1}{2}\right)^2.
}
$$

For example,

$$
15=8^2-7^2.
$$

Combining this identity with the power-of-two representation gives a formula for every positive integer $N=2^e m$, where $m$ is odd:

$$
\boxed{
N=
\frac{(1+i)^{2e}}{i^e}
\left[
\left(\frac{m+1}{2}\right)^2-
\left(\frac{m-1}{2}\right)^2
\right].
}
$$

This difference-of-squares identity is not the same as a Gaussian conjugate product. In $\mathbb Z[i]$,

$$
(a+bi)(a-bi)=a^2+b^2,
$$

because $i^2=-1$.

## 3. Gaussian conjugates and sums of two squares

An integer represented by a Gaussian conjugate pair has the form

$$
\boxed{m=(a+bi)(a-bi)=a^2+b^2}.
$$

If $m$ is odd, then $a$ and $b$ must have opposite parity: one is even and the other is odd.

If $N=2^e m$ and $m=a^2+b^2$, then

$$
\boxed{
N=
\frac{(1+i)^{2e}}{i^e}
(a+bi)(a-bi).
}
$$

Not every odd integer can be expressed as a sum of two squares. The exact criterion is the sum-of-two-squares theorem:

> A positive integer is a sum of two integer squares if and only if every prime congruent to $3\pmod4$ occurs with an even exponent in its prime factorization.

For example,

$$
45=3^2\cdot5=3^2+6^2,
$$

because the exponent of the prime $3$ is even. In contrast,

$$
21=3\cdot7
$$

is not a sum of two squares because both $3$ and $7$ are $3\pmod4$ primes occurring with odd exponents.

## 4. The two odd branches modulo $4$

Every odd positive integer belongs to one of two branches:

$$
4k+1: 1,5,9,13,17,21,25,29,\ldots
$$

or

$$
4k+3: 3,7,11,15,19,23,27,31,\ldots
$$

Every integer square is congruent to either $0$ or $1\pmod4$. Consequently, a sum of two squares can only be congruent to

$$
0,\quad1,\quad\text{or }2\pmod4,
$$

and never to $3\pmod4$. Therefore,

$$
\boxed{m\equiv3\pmod4\Longrightarrow m\neq a^2+b^2.}
$$

Numbers in the $4k+1$ branch may be sums of two squares, but membership in that branch alone is not sufficient for composite numbers.

| $m$ | Residue modulo $4$ | Sum-of-two-squares representation |
|---:|---:|:---|
| $5$ | $1$ | $1^2+2^2$ |
| $9$ | $1$ | $0^2+3^2$ |
| $13$ | $1$ | $2^2+3^2$ |
| $17$ | $1$ | $1^2+4^2$ |
| $21$ | $1$ | Impossible |
| $25$ | $1$ | $3^2+4^2$ |
| $29$ | $1$ | $2^2+5^2$ |
| $7$ | $3$ | Impossible |
| $15$ | $3$ | Impossible |
| $27$ | $3$ | Impossible |

For odd primes, the classification becomes exact:

$$
\boxed{
p\text{ is an odd prime and }p=a^2+b^2
\iff p\equiv1\pmod4.
}
$$

Primes congruent to $1\pmod4$ split into conjugate Gaussian factors:

$$
p=(a+bi)(a-bi).
$$

Examples include

$$
5=(2+i)(2-i),
$$

$$
13=(3+2i)(3-2i),
$$

and

$$
17=(4+i)(4-i).
$$

Primes congruent to $3\pmod4$, such as $3,7,11,19$, remain prime in $\mathbb Z[i]$.

## 5. Complete Gaussian prime-factor formula

Start with the ordinary prime factorization of a positive integer:

$$
N=2^{e_2}
\prod_{p\equiv1\ (4)}p^{e_p}
\prod_{q\equiv3\ (4)}q^{f_q}.
$$

Here:

- $e_2$ is the exponent of $2$;
- each $p$ is a prime congruent to $1\pmod4$;
- each $q$ is a prime congruent to $3\pmod4$.

The power-of-two formula supplies

$$
2^{e_2}=(-i)^{e_2}(1+i)^{2e_2},
$$

because $2=-i(1+i)^2$. For every prime $p\equiv1\pmod4$, the sum-of-two-squares theorem supplies integers $a_p,b_p$ such that

$$
p=a_p^2+b_p^2=(a_p+b_pi)(a_p-b_pi).
$$

A prime $q\equiv3\pmod4$ does not split into smaller Gaussian factors, so its real factor $q^{f_q}$ remains. Substituting these identities into the ordinary prime factorization produces

$$
\boxed{
N=(-i)^{e_2}(1+i)^{2e_2}
\prod_{p\equiv1\ (4)}
(a_p+b_pi)^{e_p}(a_p-b_pi)^{e_p}
\prod_{q\equiv3\ (4)}q^{f_q}.
}
$$

This formula is therefore built directly from the even-exponent identity

$$
(1+i)^{2e_2}=2^{e_2}i^{e_2}.
$$

The correcting unit $(-i)^{e_2}$ cancels $i^{e_2}$, leaving the positive real factor $2^{e_2}$.

### Trigonometric form of the complete factorization

Write

$$
\operatorname{cis}(\theta)=\cos\theta+i\sin\theta
$$

and define

$$
\theta_p=\operatorname{atan2}(b_p,a_p).
$$

The factors then have the polar forms

$$
(-i)^{e_2}=\operatorname{cis}\left(-\frac{e_2\pi}{2}\right),
$$

$$
(1+i)^{2e_2}
=2^{e_2}\operatorname{cis}\left(\frac{e_2\pi}{2}\right),
$$

and

$$
(a_p\mathbin{\pm}b_pi)^{e_p}
=p^{e_p/2}\operatorname{cis}(\mathbin{\pm}e_p\theta_p).
$$

Thus the complete sine-and-cosine representation is

$$
\boxed{
\begin{aligned}
N={}&
2^{e_2}
\left[\cos\left(-\frac{e_2\pi}{2}\right)
+i\sin\left(-\frac{e_2\pi}{2}\right)\right]
\left[\cos\left(\frac{e_2\pi}{2}\right)
+i\sin\left(\frac{e_2\pi}{2}\right)\right]\\
&\times
\prod_{p\equiv1\ (4)}p^{e_p}
\left[\cos(e_p\theta_p)+i\sin(e_p\theta_p)\right]
\left[\cos(-e_p\theta_p)+i\sin(-e_p\theta_p)\right]\\
&\times
\prod_{q\equiv3\ (4)}q^{f_q}.
\end{aligned}}
$$

All angles cancel in opposite pairs:

$$
-\frac{e_2\pi}{2}+\frac{e_2\pi}{2}=0
$$

and

$$
e_p\theta_p-e_p\theta_p=0.
$$

The remaining magnitudes reproduce the ordinary prime factorization:

$$
N=
2^{e_2}
\prod_{p\equiv1\ (4)}p^{e_p}
\prod_{q\equiv3\ (4)}q^{f_q}
[\cos0+i\sin0].
$$

Since $\cos0+i\sin0=1$, the final result lies on the positive real axis.

## 6. Polar form and cancelling rotations

If

$$
p=a^2+b^2
$$

and

$$
\theta=\operatorname{atan2}(b,a),
$$

then

$$
a+bi=\sqrt p(\cos\theta+i\sin\theta)
$$

and

$$
a-bi=\sqrt p(\cos(-\theta)+i\sin(-\theta)).
$$

Their product has magnitude $p$ and total angle zero:

$$
(a+bi)(a-bi)
=p[\cos0+i\sin0]
=p.
$$

For example,

$$
65=(2+i)(2-i)(3+2i)(3-2i).
$$

The first conjugate pair produces $5$, and the second produces $13$:

$$
(2+i)(2-i)=5,
$$

$$
(3+2i)(3-2i)=13.
$$

Hence,

$$
65=5\cdot13
$$

and

$$
65\equiv0\pmod{13}.
$$

The Gaussian factorization does not provide a different reason for divisibility by $13$. Instead, it exposes the factor $13$ as a product of two conjugate Gaussian integers whose rotations cancel.

## 7. Even numbers as sums of two odd numbers

Every even integer $N$ can be written as a sum of two odd integers:

$$
\boxed{N=r+s},
$$

where $r$ and $s$ are odd. The simplest universal choice is

$$
N=1+(N-1).
$$

Since $N$ is even, $N-1$ is odd.

This additive parity fact is connected to the Gaussian factor $1+i$. Place the two odd summands into the coordinates of a Gaussian integer:

$$
z=r+si.
$$

Dividing by $1+i$ gives

$$
\begin{aligned}
\frac{r+si}{1+i}
&=\frac{(r+si)(1-i)}{2}\\
&=\frac{r+s}{2}+\frac{s-r}{2}i\\
&=\frac N2+\frac{s-r}{2}i.
\end{aligned}
$$

Because $r$ and $s$ are both odd, their sum and difference are both even. Therefore,

$$
\boxed{
\frac{r+si}{1+i}
=\frac N2+\frac{s-r}{2}i
\in\mathbb Z[i].
}
$$

Equivalently,

$$
\boxed{
r+si=(1+i)
\left(
\frac N2+\frac{s-r}{2}i
\right).
}
$$

### The coordinate transformation

Multiplication by $1+i$ transforms Gaussian coordinates according to

$$
(1+i)(a+bi)=(a-b)+(a+b)i.
$$

Thus,

$$
\boxed{(a,b)\longmapsto(a-b,a+b)}.
$$

Geometrically, this is a counterclockwise rotation by $45^\circ$, together with scaling by $\sqrt2$. The two resulting coordinates have the same parity because

$$
(a+b)-(a-b)=2b.
$$

Conversely, when two coordinates $r,s$ have the same parity, the inverse transformation

$$
(r,s)\longmapsto
\left(\frac{r+s}{2},\frac{s-r}{2}\right)
$$

produces integer coordinates. This establishes the Gaussian divisibility criterion

$$
\boxed{
1+i\mid(r+si)
\iff
r\text{ and }s\text{ have the same parity}.
}
$$

When $r,s$ are odd, their sum $N=r+s$ is even. Dividing by $1+i$ performs a clockwise rotation by $45^\circ$ and makes $N/2$ the new real coordinate.

For example,

$$
10=3+7.
$$

Placing the summands into $3+7i$ gives

$$
\frac{3+7i}{1+i}
=\frac{3+7}{2}+\frac{7-3}{2}i
=5+2i.
$$

Hence,

$$
\boxed{3+7i=(1+i)(5+2i)}.
$$

The new real coordinate $5$ is half of the original even sum $10$.

### Distinctions from stronger statements

The fact that every even integer is a sum of two odd integers does not mean that every even integer is a sum of two odd squares. Since every odd square is congruent to $1\pmod8$,

$$
\text{odd}^2+\text{odd}^2\equiv2\pmod8.
$$

Therefore, only numbers congruent to $2\pmod8$ can possibly be sums of two odd squares.

Requiring the two odd summands to be prime is also a much stronger statement: it is Goldbach's conjecture, not merely the elementary parity identity above.

## 8. Relation to Goldbach decompositions

Goldbach's conjecture concerns additive decompositions

$$
X=P+Q,
$$

where $X>2$ is even and $P,Q$ are primes. Whether a prime can itself be written as a sum of two squares is a separate property. In particular, a prime $q\equiv3\pmod4$ cannot be a sum of two squares, but it can still be a valid Goldbach summand.

For example,

$$
14=7+7,
$$

even though $7\equiv3\pmod4$ and $7\neq a^2+b^2$ for all integers $a,b$.

For even $X$ expressed as the sum of two odd primes, modular arithmetic determines the possible residue pairs:

| $X\bmod4$ | Possible $(P\bmod4,Q\bmod4)$ |
|---:|:---|
| $0$ | $(1,3)$ or $(3,1)$ |
| $2$ | $(1,1)$ or $(3,3)$ |

Thus, restricting both Goldbach summands to the $1\pmod4$ branch would omit valid decompositions and cannot handle numbers congruent to $0\pmod4$.

The two prime branches can nevertheless be translated using the square identities developed above.

### Two primes congruent to $1\pmod4$

If

$$
P=a^2+b^2,
\qquad
Q=c^2+d^2,
$$

then

$$
\boxed{X=P+Q=a^2+b^2+c^2+d^2.}
$$

This case necessarily has $X\equiv2\pmod4$. For example,

$$
18=5+13=1^2+2^2+2^2+3^2.
$$

### One prime from each branch

Let $P\equiv1\pmod4$ and $Q\equiv3\pmod4$. Write

$$
P=a^2+b^2
$$

and use the difference-of-consecutive-squares identity

$$
Q=
\left(\frac{Q+1}{2}\right)^2-
\left(\frac{Q-1}{2}\right)^2.
$$

Then

$$
\boxed{
X=a^2+b^2+
\left(\frac{Q+1}{2}\right)^2-
\left(\frac{Q-1}{2}\right)^2.
}
$$

This case has $X\equiv0\pmod4$. For example,

$$
12=5+7=1^2+2^2+4^2-3^2.
$$

### Two primes congruent to $3\pmod4$

For $Q_1,Q_2\equiv3\pmod4$, write each prime as a difference of consecutive squares. This gives

$$
\boxed{
\begin{aligned}
X={}&
\left(\frac{Q_1+1}{2}\right)^2+
\left(\frac{Q_2+1}{2}\right)^2\\
&-
\left(\frac{Q_1-1}{2}\right)^2-
\left(\frac{Q_2-1}{2}\right)^2.
\end{aligned}}
$$

This case also has $X\equiv2\pmod4$. For example,

$$
14=7+7=(4^2-3^2)+(4^2-3^2),
$$

so

$$
\boxed{14=4^2+4^2-3^2-3^2.}
$$

These formulas translate an already known Goldbach decomposition into sums and differences of squares. They do not prove that every even integer possesses a Goldbach decomposition; that existence statement remains Goldbach's conjecture.

## 9. When the branch formulas reduce to two squares

The four-square and signed-four-square formulas obtained from a Goldbach decomposition do not automatically reduce to a sum of two squares. The decisive restriction applies to the prime factorization of the final number $X$:

$$
\boxed{
X=A^2+B^2
\iff
\text{every prime }q\equiv3\pmod4
\text{ occurs in }X\text{ with an even exponent}.
}
$$

Relations among the square variables can provide simple direct reductions, but they are sufficient conditions rather than the complete criterion.

### Two primes from the $1\pmod4$ branch

Suppose

$$
P=a^2+b^2,
\qquad
Q=c^2+d^2,
$$

where $a,b$ have opposite parity and $c,d$ have opposite parity. Then

$$
X=P+Q=a^2+b^2+c^2+d^2.
$$

Since $P,Q\equiv1\pmod4$,

$$
X\equiv2\pmod4.
$$

If $X=A^2+B^2$, then $A$ and $B$ must both be odd:

$$
\boxed{A\equiv B\equiv1\pmod2.}
$$

The opposite parity of each original pair does not by itself guarantee that four squares reduce to two. For example,

$$
18=5+13=1^2+2^2+2^2+3^2
$$

does reduce:

$$
\boxed{18=3^2+3^2}.
$$

In contrast,

$$
42=5+37=1^2+2^2+1^2+6^2
$$

does not reduce to two squares because

$$
42=2\cdot3\cdot7
$$

contains the primes $3,7\equiv3\pmod4$ with odd exponents.

### One prime from each branch

Suppose

$$
P=a^2+b^2,
\qquad
Q=c^2-d^2,
$$

where $P\equiv1\pmod4$, $Q\equiv3\pmod4$, and $c,d$ are consecutive. Then

$$
X=a^2+b^2+c^2-d^2.
$$

Since

$$
X\equiv1+3\equiv0\pmod4,
$$

any two-square representation of $X$ must have both coordinates even:

$$
\boxed{X=A^2+B^2\Longrightarrow A\equiv B\equiv0\pmod2.}
$$

Consequently,

$$
\frac X4=left(\frac A2\right)^2+left(\frac B2\right)^2.
$$

A simple sufficient relation among the original variables is

$$
\boxed{b=d}.
$$

In that case, the positive and negative copies of $b^2$ cancel:

$$
a^2+b^2+c^2-d^2=a^2+c^2.
$$

For example,

$$
20=13+7
$$

with

$$
13=2^2+3^2,
\qquad
7=4^2-3^2.
$$

Therefore,

$$
20=2^2+3^2+4^2-3^2
=\boxed{2^2+4^2}.
$$

Direct cancellation is not necessary, however; the complete test remains the prime-exponent condition. Conversely, not every mixed-branch expression reduces. For example,

$$
12=5+7=1^2+2^2+4^2-3^2,
$$

but $12=2^2\cdot3$ contains $3\equiv3\pmod4$ to an odd power, so $12$ is not a sum of two squares.

### Two primes from the $3\pmod4$ branch

Write

$$
Q_1=a^2-b^2,
\qquad
Q_2=c^2-d^2.
$$

Then

$$
X=a^2+c^2-b^2-d^2.
$$

Since

$$
X\equiv3+3\equiv2\pmod4,
$$

a two-square representation, if one exists, must again use two odd coordinates:

$$
\boxed{X=A^2+B^2\Longrightarrow A,B\text{ are odd}.}
$$

For example,

$$
18=7+11=(4^2-3^2)+(6^2-5^2).
$$

The signed squares do not directly cancel, but

$$
18=2\cdot3^2
$$

contains its $3\pmod4$ prime to an even power. Hence,

$$
\boxed{18=3^2+3^2}.
$$

On the other hand,

$$
14=7+7=2\cdot7
$$

contains $7\equiv3\pmod4$ to an odd power and cannot be represented as a sum of two squares.

The complete conclusion is

$$
\boxed{
\begin{aligned}
&\text{relations such as }b=d\text{ can produce direct cancellation, but}\\
&X\text{ reduces to two squares exactly when every }q\equiv3\pmod4\\
&\text{has an even exponent in the prime factorization of }X.
\end{aligned}}
$$

## 10. What the Gaussian framework adds to Goldbach

Gaussian factorization gives Goldbach decompositions additional structure and useful restrictions, although it does not prove Goldbach's conjecture.

For

$$
X=P+Q,
$$

the Gaussian viewpoint separates odd primes into two branches:

$$
p\equiv1\pmod4
\Longrightarrow
p=(a+bi)(a-bi)=a^2+b^2,
$$

while a prime $q\equiv3\pmod4$ does not split in $\mathbb Z[i]$ and can instead be translated using a difference of consecutive squares.

This framework contributes the following constraints.

### 1. The residue of $X$ restricts the prime branches

$$
\boxed{
\begin{array}{c|c}
X\bmod4&(P\bmod4,Q\bmod4)\\ \hline
0&(1,3)\text{ or }(3,1)\\
2&(1,1)\text{ or }(3,3)
\end{array}}
$$

Thus an even number congruent to $0\pmod4$ requires one odd prime from each branch, while an even number congruent to $2\pmod4$ requires two odd primes from the same branch.

### 2. Split primes impose coordinate parity

If both primes are congruent to $1\pmod4$, then

$$
X=a^2+b^2+c^2+d^2,
$$

where $a,b$ have opposite parity and $c,d$ have opposite parity. This follows because each odd sum of two squares contains one even square and one odd square.

### 3. Reduction to two squares imposes a factorization condition

If the final number is also required to satisfy

$$
X=A^2+B^2,
$$

then every prime $q\equiv3\pmod4$ in the prime factorization of $X$ must have an even exponent.

The parity of the final coordinates is also determined by $X$:

$$
X\equiv2\pmod4
\Longrightarrow
A,B\text{ are odd},
$$

whereas

$$
X\equiv0\pmod4
\Longrightarrow
A,B\text{ are even}.
$$

### 4. Relations among coordinates can force direct reduction

In a mixed-branch expression

$$
X=a^2+b^2+c^2-d^2,
$$

a relation such as

$$
b=d
$$

causes direct cancellation and gives

$$
X=a^2+c^2.
$$

This is a useful sufficient condition, although the full necessary-and-sufficient condition remains the prime-exponent test for $X$.

### 5. The factor $1+i$ records parity geometrically

The Gaussian divisibility relation

$$
1+i\mid(r+si)
\iff
r\equiv s\pmod2
$$

encodes the equal-parity relationship between two coordinates. Multiplication or division by $1+i$ expresses this parity relation as a $45^\circ$ rotation and a scaling by $\sqrt2$.

Consequently, Gaussian integers provide a structured coordinate system for studying Goldbach decompositions through residue classes, parity, rotations, norms, and factorization. The logical boundary is

$$
\boxed{
\text{Gaussian factorization constrains and classifies possible Goldbach decompositions,}
}
$$

but

$$
\boxed{
\text{it does not prove that a prime pair exists for every even }X.
}
$$

## 11. Refining the branches modulo $8$ and adding dimensions

Passing from modulo $4$ to modulo $8$ refines the two odd branches, but it does not switch their Gaussian behavior. The odd residue classes modulo $8$ are

$$
1,\quad3,\quad5,\quad7.
$$

Their relationship with the modulo-$4$ branches is

$$
\boxed{
\begin{array}{c|c}
p\bmod4&p\bmod8\\ \hline
1&1\text{ or }5\\
3&3\text{ or }7
\end{array}}
$$

Consequently, for an odd prime $p$:

- $p\equiv1$ or $5\pmod8$ splits into Gaussian conjugate factors;
- $p\equiv3$ or $7\pmod8$ remains prime in $\mathbb Z[i]$.

Equivalently,

$$
\boxed{
p=a^2+b^2
\iff
p\equiv1\text{ or }5\pmod8
}
$$

for odd primes.

### What modulo $8$ says about the coordinates

If an odd prime satisfies

$$
p=a^2+b^2,
$$

then one of $a,b$ is odd and the other is even. An odd square is $1\pmod8$, while an even square is either $0$ or $4\pmod8$. Therefore:

- if $p\equiv1\pmod8$, the even coordinate is divisible by $4$;
- if $p\equiv5\pmod8$, the even coordinate is congruent to $2\pmod4$.

For example,

$$
17=4^2+1^2,
\qquad
17\equiv1\pmod8,
$$

where the even coordinate $4$ is divisible by $4$. In contrast,

$$
13=2^2+3^2,
\qquad
13\equiv5\pmod8,
$$

where the even coordinate $2$ is $2\pmod4$.

Thus modulo $8$ provides finer coordinate information, but it does not make the $3\pmod4$ branch split in the Gaussian integers.

### A hyperbolic extension: split-complex numbers

Every odd integer can be represented as a difference of two consecutive squares. This can be encoded multiplicatively by introducing a split-complex unit $j$ satisfying

$$
j^2=1.
$$

Then

$$
(a+bj)(a-bj)=a^2-b^2.
$$

For example,

$$
7=4^2-3^2=(4+3j)(4-3j).
$$

This is not an additional Euclidean rotation like multiplication by $i$. Split-complex geometry has a hyperbolic norm $a^2-b^2$, which can be positive, negative, or zero.

### Euclidean orthogonal extensions: three and four squares

If positive orthogonal square coordinates are required, extra dimensions provide a different extension. A number represented by

$$
a^2+b^2+c^2
$$

is the squared Euclidean length of a three-dimensional integer vector. Legendre's three-square theorem states that a positive integer has such a representation exactly when it is not of the form

$$
4^r(8s+7).
$$

Therefore, a prime congruent to $3\pmod8$ can be represented by three squares. For example,

$$
3=1^2+1^2+1^2
$$

and

$$
19=3^2+3^2+1^2.
$$

A prime congruent to $7\pmod8$ cannot be represented by three squares and requires four. For example,

$$
\boxed{7=2^2+1^2+1^2+1^2}.
$$

Lagrange's four-square theorem guarantees that every nonnegative integer is a sum of four integer squares. The four-square expression is naturally the norm of a quaternion:

$$
q=a+bi+cj+dk,
$$

with

$$
\operatorname N(q)=a^2+b^2+c^2+d^2.
$$

For instance,

$$
\boxed{
\operatorname N(2+i+j+k)
=2^2+1^2+1^2+1^2
=7.
}
$$

The relevant number systems and their norm forms can therefore be summarized as follows:

| Number system | Norm form | Geometric character |
|:---|:---|:---|
| Complex/Gaussian | $a^2+b^2$ | Two-dimensional Euclidean |
| Split-complex | $a^2-b^2$ | Two-dimensional hyperbolic |
| Quaternions | $a^2+b^2+c^2+d^2$ | Four-dimensional Euclidean |

Modulo $8$ reveals when two or three positive square coordinates are insufficient. The quaternion extension supplies enough Euclidean orthogonal coordinates to represent every positive integer, including primes that remain unsplit in $\mathbb Z[i]$.

## 12. Using the split-complex unit $j$ for both odd branches

Let $j$ be the split-complex unit satisfying

$$
j^2=1.
$$

Unlike the Gaussian identity

$$
(a+bi)(a-bi)=a^2+b^2,
$$

split-complex conjugation produces a difference of squares:

$$
\boxed{(a+bj)(a-bj)=a^2-b^2.}
$$

Every odd positive integer $N$, in either modulo-$4$ branch, can be represented this way. Set

$$
A=\frac{N+1}{2},
\qquad
B=\frac{N-1}{2}.
$$

Since $A$ and $B$ are consecutive integers,

$$
A^2-B^2=(A+B)(A-B)=N\cdot1=N.
$$

Therefore,

$$
\boxed{
N=(A+Bj)(A-Bj),
\qquad
A=\frac{N+1}{2},\quad B=\frac{N-1}{2}.
}
$$

For a number in the $1\pmod4$ branch,

$$
5=3^2-2^2=(3+2j)(3-2j),
$$

and

$$
13=7^2-6^2=(7+6j)(7-6j).
$$

For a number in the $3\pmod4$ branch,

$$
7=4^2-3^2=(4+3j)(4-3j),
$$

and

$$
11=6^2-5^2=(6+5j)(6-5j).
$$

Thus both odd branches admit split-complex conjugate products. This universality is different from Gaussian splitting: it expresses every odd number as a difference of squares and consequently does not distinguish primes from composites.

### Hyperbolic-angle form

The split-complex analogue of the circular expression

$$
\cos\theta+i\sin\theta
$$

is

$$
\cosh t+j\sinh t.
$$

For $N>0$, set

$$
t=\frac12\ln N.
$$

Then

$$
\sqrt N\cosh t=\frac{N+1}{2}=A
$$

and

$$
\sqrt N\sinh t=\frac{N-1}{2}=B.
$$

Consequently,

$$
A\mathbin{\pm}Bj
=\sqrt N(\cosh t\mathbin{\pm}j\sinh t),
$$

and the universal hyperbolic representation is

$$
\boxed{
N=
\sqrt N(\cosh t+j\sinh t)
\sqrt N(\cosh t-j\sinh t),
\qquad
t=\frac12\ln N.
}
$$

This follows from

$$
\cosh^2t-\sinh^2t=1.
$$

### Comparing $\mathbb Z[i]$ and $\mathbb Z[j]$

Write

$$
\mathbb Z[i]=\{a+bi:a,b\in\mathbb Z,\ i^2=-1\}
$$

and

$$
\mathbb Z[j]=\{a+bj:a,b\in\mathbb Z,\ j^2=1\}.
$$

The second ring is the ring of integer split-complex numbers. Their relevant properties are:

| Property | Gaussian integers $\mathbb Z[i]$ | Split-complex integers $\mathbb Z[j]$ |
|:---|:---|:---|
| Defining relation | $i^2=-1$ | $j^2=1$ |
| Conjugate | $a-bi$ | $a-bj$ |
| Conjugate product | $a^2+b^2$ | $a^2-b^2$ |
| Geometry | Circular/Euclidean | Hyperbolic |
| Basic functions | $\cos\theta+i\sin\theta$ | $\cosh t+j\sinh t$ |
| Odd $1\pmod4$ prime | Splits as a sum of two squares | Always a difference of consecutive squares |
| Odd $3\pmod4$ prime | Does not split | Always a difference of consecutive squares |
| Ability to detect $N=a^2+b^2$ | Yes: this is exactly its norm form | No: its norm form is a difference, not a sum |
| Universal odd representation | No | Yes, as $A^2-B^2$ |
| Zero divisors | None | Yes: $(1+j)(1-j)=0$ |

The ability to represent sums of two squares therefore belongs naturally to $\mathbb Z[i]$:

$$
\boxed{
N=a^2+b^2
\iff
N=(a+bi)(a-bi)
\text{ in }\mathbb Z[i].
}
$$

The corresponding statement in $\mathbb Z[j]$ concerns differences:

$$
\boxed{
N=a^2-b^2
\iff
N=(a+bj)(a-bj)
\text{ in }\mathbb Z[j].
}
$$

Because $\mathbb Z[j]$ has zero divisors and gives every odd number the same consecutive-square construction, its universal representation does not carry the same prime-splitting information as Gaussian factorization. The two systems are complementary:

- $\mathbb Z[i]$ distinguishes the $1\pmod4$ and $3\pmod4$ prime branches through sums of squares;
- $\mathbb Z[j]$ unifies both odd branches through differences of squares.

## 13. A scaled imaginary unit with $h^2=-1/2$

Consider a unit $h$ satisfying

$$
h^2=-\frac12.
$$

Inside the ordinary complex numbers, its two possible values are

$$
\boxed{h=\mathbin{\pm}\frac{i}{\sqrt2}}.
$$

Indeed,

$$
\left(\frac{i}{\sqrt2}\right)^2
=\frac{i^2}{2}
=-\frac12.
$$

Thus $h$ is not a new independent imaginary direction; it is the ordinary imaginary unit scaled by $1/\sqrt2$.

For

$$
z=a+bh=a+\frac{b}{\sqrt2}i,
$$

the conjugate is

$$
\overline z=a-bh,
$$

and the conjugate product is

$$
\boxed{
z\overline z
=(a+bh)(a-bh)
=a^2+\frac{b^2}{2}.
}
$$

Unlike the positive unit relations $j^2=1$ and $k^2=1/2$, the negative sign in $h^2=-1/2$ produces a positive weighted sum of squares.

### The integral form $a^2+2c^2$

If $a,b\in\mathbb Z$, then $a^2+b^2/2$ is an integer only when $b$ is even. Write

$$
b=2c.
$$

Then

$$
a+bh=a+2ch=a+c\sqrt2\,i
$$

and

$$
\boxed{z\overline z=a^2+2c^2.}
$$

It is convenient to rescale the unit by defining

$$
v=2h=\sqrt2\,i.
$$

This gives

$$
\boxed{v^2=-2}.
$$

The corresponding integral quadratic ring is

$$
\mathbb Z[\sqrt{-2}]
=\{a+cv:a,c\in\mathbb Z\},
$$

whose norm is

$$
\boxed{
(a+cv)(a-cv)=a^2+2c^2.
}
$$

Using $v$ rather than $h$ avoids the halves introduced by multiplying arbitrary integer combinations of $1$ and $h$.

### Prime branches represented by $a^2+2c^2$

For an odd prime $p$,

$$
\boxed{
p=a^2+2c^2
\iff
p\equiv1\text{ or }3\pmod8.
}
$$

Examples include

$$
3=1^2+2(1^2),
$$

$$
11=3^2+2(1^2),
$$

$$
17=3^2+2(2^2),
$$

and

$$
19=1^2+2(3^2).
$$

Correspondingly,

$$
3=(1+\sqrt{-2})(1-\sqrt{-2}),
$$

$$
11=(3+\sqrt{-2})(3-\sqrt{-2}),
$$

and

$$
17=(3+2\sqrt{-2})(3-2\sqrt{-2}).
$$

Odd primes congruent to $5$ or $7\pmod8$ cannot be represented by the form $a^2+2c^2$.

### Why modulo $4$ is not sufficient

Suppose an odd prime has a representation

$$
p=a^2+2c^2.
$$

Since $2c^2$ is even and $p$ is odd, $a$ must be odd. Therefore,

$$
a^2\equiv1\pmod4.
$$

The second term depends on the parity of $c$:

$$
2c^2\equiv
\begin{cases}
0\pmod4,&c\text{ even},\\
2\pmod4,&c\text{ odd}.
\end{cases}
$$

It follows that

$$
a^2+2c^2\equiv
\begin{cases}
1\pmod4,&c\text{ even},\\
3\pmod4,&c\text{ odd}.
\end{cases}
$$

Thus the norm $a^2+2c^2$ can represent primes from both modulo-$4$ branches:

$$
\boxed{
\begin{aligned}
c\text{ even}&\Longrightarrow p\equiv1\pmod4,\\
c\text{ odd}&\Longrightarrow p\equiv3\pmod4.
\end{aligned}}
$$

Modulo $4$ alone cannot determine which primes in those branches are representable. Modulo $8$ supplies the required refinement:

| $p\bmod4$ | $p\bmod8$ | Can an odd prime have $p=a^2+2c^2$? |
|---:|---:|:---|
| $1$ | $1$ | Yes |
| $1$ | $5$ | No |
| $3$ | $3$ | Yes |
| $3$ | $7$ | No |

For example, in the $1\pmod4$ branch,

$$
17\equiv1\pmod8,
\qquad
17=3^2+2(2^2),
$$

whereas $13\equiv5\pmod8$ cannot be represented by this form.

In the $3\pmod4$ branch,

$$
11\equiv3\pmod8,
\qquad
11=3^2+2(1^2),
$$

whereas $7\equiv7\pmod8$ cannot be represented by this form.

Therefore,

$$
\boxed{
\text{modulo }4\text{ identifies the parity of }c,
\text{ while modulo }8\text{ determines prime representability}.
}
$$

The form $a^2+2c^2$ selects half of each modulo-$4$ branch: $1\pmod8$ from the $1\pmod4$ branch and $3\pmod8$ from the $3\pmod4$ branch.

### Comparison with the Gaussian norm

The two positive quadratic norm forms capture different prime residue branches:

| Quadratic norm | Defining unit | Odd prime residues represented |
|:---|:---|:---|
| $a^2+b^2$ | $i^2=-1$ | $1,5\pmod8$ |
| $a^2+2c^2$ | $v^2=-2$ | $1,3\pmod8$ |

Thus the scaled imaginary construction captures the $3\pmod8$ prime branch that the Gaussian sum-of-two-squares norm does not capture. It still does not represent primes congruent to $7\pmod8$, which require a different quadratic form or additional positive-square dimensions.

## 14. A square root of $i$: $h^2=i$

In this section the symbol $h$ is redefined. To distinguish it from the scaled imaginary unit of the preceding section, that earlier unit is denoted here by $h_0=i/\sqrt2$.

If

$$
h^2=i,
$$

then the two square roots of $i$ are

$$
\boxed{h=\mathbin{\pm}\frac{1+i}{\sqrt2}}.
$$

Choosing the positive root gives

$$
h=\frac1{\sqrt2}+\frac{i}{\sqrt2}
=\cos\frac{\pi}{4}+i\sin\frac{\pi}{4}
=e^{i\pi/4}.
$$

If the previous scaled imaginary unit is denoted by

$$
h_0=\frac{i}{\sqrt2},
\qquad
h_0^2=-\frac12,
$$

then, numerically,

$$
\boxed{h=h_0+\frac1{\sqrt2}}.
$$

Thus $h$ is obtained by shifting $h_0$ horizontally by $1/\sqrt2$. Its more important geometric property is that it is a unit complex number representing a pure $45^\circ$ rotation.

Its powers satisfy

$$
\begin{aligned}
h^0&=1,\\
h^1&=\frac{1+i}{\sqrt2},\\
h^2&=i,\\
h^3&=\frac{-1+i}{\sqrt2},\\
h^4&=-1,\\
h^8&=1.
\end{aligned}
$$

Consequently,

$$
\boxed{
h^x=\cos\frac{x\pi}{4}+i\sin\frac{x\pi}{4}.
}
$$

This unit is directly related to the original factor $1+i$:

$$
1+i=\sqrt2\,h.
$$

Therefore,

$$
\boxed{(1+i)^x=2^{x/2}h^x.}
$$

The factor $h^x$ supplies the rotation, while $2^{x/2}$ supplies the scaling.

### The complex norm of $a+bh$

Since

$$
\overline h=\frac{1-i}{\sqrt2}=h^{-1},
$$

the ordinary complex magnitude squared is

$$
\begin{aligned}
|a+bh|^2
&=(a+bh)(a+b\overline h)\\
&=a^2+ab(h+\overline h)+b^2h\overline h\\
&=a^2+\sqrt2\,ab+b^2.
\end{aligned}
$$

Hence,

$$
\boxed{|a+bh|^2=a^2+\sqrt2\,ab+b^2.}
$$

Unlike $a^2+b^2$, this expression generally contains an irrational cross term when $a,b\in\mathbb Z$.

### The closed ring generated by $h$

The two-dimensional set

$$
\{a+bh:a,b\in\mathbb Z\}
$$

is not closed under multiplication because $h^2=i$ cannot generally be written as $a+bh$ with integer $a,b$. Since

$$
h^2=i,
\qquad
h^4=-1,
\qquad
h^8=1,
$$

the proper closed integer ring is

$$
\boxed{
\mathbb Z[h]
=\{a+bh+ch^2+dh^3:a,b,c,d\in\mathbb Z\}.
}
$$

This is the ring of eighth cyclotomic integers,

$$
\mathbb Z[\zeta_8].
$$

### The complete algebraic norm

For the simpler element $a+bh$, the complete algebraic norm across all four conjugates is

$$
\boxed{
\operatorname N_{\mathbb Q(h)/\mathbb Q}(a+bh)=a^4+b^4.
}
$$

This is automatically a sum of two squares:

$$
\boxed{a^4+b^4=(a^2)^2+(b^2)^2.}
$$

The new unit therefore produces two related norm expressions:

| Norm | Result |
|:---|:---|
| Ordinary complex magnitude squared | $a^2+\sqrt2ab+b^2$ |
| Complete algebraic norm | $a^4+b^4$ |

The central geometric result is that

$$
h=\frac{1+i}{\sqrt2}
$$

isolates the rotational part of $1+i$: it rotates by $45^\circ$ without changing magnitude.

## 15. Extracting the Gaussian subring from the cyclotomic extension

Let the normalized $45^\circ$ rotational unit be

$$
r=\frac{1+i}{\sqrt2}
=\cos\frac{\pi}{4}+i\sin\frac{\pi}{4}
=\zeta_8.
$$

Squaring this unit gives

$$
\begin{aligned}
r^2
&=\left(\frac{1+i}{\sqrt2}\right)^2\\
&=\frac{(1+i)^2}{2}\\
&=\frac{1+2i+i^2}{2}\\
&=i.
\end{aligned}
$$

If

$$
h=r^2,
$$

then

$$
\boxed{h=i}
$$

and consequently

$$
\boxed{h^2=-1}.
$$

Geometrically, $r$ rotates by $45^\circ$, whereas $h=r^2=i$ rotates by $90^\circ$. Its powers follow the four-step Gaussian cycle:

$$
\begin{aligned}
h^0&=1,\\
h^1&=i,\\
h^2&=-1,\\
h^3&=-i,\\
h^4&=1.
\end{aligned}
$$

### Returning to the Gaussian norm

For

$$
z=a+bh=a+bi,
$$

the conjugate and norm are

$$
\overline z=a-bi
$$

and

$$
\boxed{
z\overline z
=(a+bi)(a-bi)
=a^2+b^2.
}
$$

Thus the ring generated by the squared rotational unit is exactly

$$
\boxed{\mathbb Z[h]=\mathbb Z[i].}
$$

This recovers the ordinary Gaussian prime classification:

$$
\boxed{
p=a^2+b^2
\iff
p\equiv1\pmod4
}
$$

for odd primes, or equivalently

$$
p\equiv1\text{ or }5\pmod8.
$$

### Recovering the even and odd power formulas

Since

$$
1+i=\sqrt2\,r
$$

and $r^2=h=i$, an even exponent $x=2n$ gives

$$
\begin{aligned}
(1+i)^{2n}
&=(\sqrt2\,r)^{2n}\\
&=2^n r^{2n}\\
&=2^n h^n\\
&=2^n i^n.
\end{aligned}
$$

Therefore,

$$
\boxed{(1+i)^{2n}=2^n i^n.}
$$

For an odd exponent, one $45^\circ$ factor remains:

$$
\boxed{
(1+i)^{2n+1}=2^n i^n(1+i).
}
$$

This explains why even powers lie on the coordinate axes while odd powers lie on the diagonal directions.

### The ring relationship

The eighth-cyclotomic ring is

$$
\mathbb Z[\zeta_8]=\mathbb Z[r],
$$

whereas its subring generated by the square of $r$ is

$$
\mathbb Z[r^2]=\mathbb Z[i].
$$

Hence,

$$
\boxed{
\mathbb Z[i]=\mathbb Z[r^2]\subset\mathbb Z[r]=\mathbb Z[\zeta_8].
}
$$

The containment is proper: $r=(1+i)/\sqrt2$ belongs to $\mathbb Z[\zeta_8]$ but not to $\mathbb Z[i]$. Restricting from all powers of $r$ to its even powers removes the extra $45^\circ$ directions and leaves the $90^\circ$ Gaussian rotations.

Thus squaring the cyclotomic generator does not define a ring homomorphism on every element. Rather, it selects the Gaussian subring generated by its square:

$$
\boxed{
r=\zeta_8
\quad\Longrightarrow\quad
r^2=i,
\qquad
\mathbb Z[r^2]=\mathbb Z[i].
}
$$

## 16. Using the third-power cyclotomic generator

Let

$$
r=\frac{1+i}{\sqrt2}=e^{i\pi/4}=\zeta_8
$$

and define

$$
h=r^3
=\left(\frac1{\sqrt2}+\frac{i}{\sqrt2}\right)^3.
$$

Then

$$
h=e^{3i\pi/4},
$$

so

$$
\boxed{
h=\cos\frac{3\pi}{4}+i\sin\frac{3\pi}{4}
=\frac{-1+i}{\sqrt2}.
}
$$

Thus $h$ is a pure counterclockwise rotation by $135^\circ$. It can also be written as

$$
\boxed{h=ir},
$$

because

$$
i\frac{1+i}{\sqrt2}
=\frac{-1+i}{\sqrt2}.
$$

### Powers and rotational order

Squaring gives

$$
\boxed{h^2=-i}.
$$

The first powers are

$$
\begin{aligned}
h^0&=1,\\
h^1&=\frac{-1+i}{\sqrt2},\\
h^2&=-i,\\
h^3&=\frac{1+i}{\sqrt2}=r,\\
h^4&=-1,\\
h^8&=1.
\end{aligned}
$$

Because $3$ is relatively prime to $8$, repeated multiplication by $h$ visits all eight eighth-root directions, but in a different order from repeated multiplication by $r$.

Furthermore,

$$
\boxed{r=h^3},
$$

since

$$
h^3=r^9=r
$$

using $r^8=1$.

### Relation to $1+i$

Since

$$
1+i=\sqrt2\,r
$$

and $r=h^3$,

$$
\boxed{1+i=\sqrt2\,h^3}.
$$

Therefore,

$$
\boxed{(1+i)^x=2^{x/2}h^{3x}.}
$$

For an even exponent $x=2n$,

$$
(1+i)^{2n}=2^n h^{6n}.
$$

Because

$$
h^6=(h^2)^3=(-i)^3=i,
$$

the original identity is recovered:

$$
\boxed{(1+i)^{2n}=2^n i^n.}
$$

Using the third-power generator therefore leaves the power-of-two formula unchanged and only reorders the eight rotational directions.

### Norm of $a+bh$

The complex conjugate of $h$ is

$$
\overline h=\frac{-1-i}{\sqrt2}=h^{-1}.
$$

Since

$$
h+\overline h=-\sqrt2
$$

and

$$
h\overline h=1,
$$

the ordinary complex magnitude squared is

$$
\begin{aligned}
|a+bh|^2
&=(a+bh)(a+b\overline h)\\
&=a^2+ab(h+\overline h)+b^2\\
&=a^2-\sqrt2\,ab+b^2.
\end{aligned}
$$

Hence,

$$
\boxed{|a+bh|^2=a^2-\sqrt2\,ab+b^2.}
$$

The sign of the cross term is reversed from the corresponding expression for $r$:

$$
|a+br|^2=a^2+\sqrt2\,ab+b^2.
$$

The complete algebraic norm, however, remains

$$
\boxed{
\operatorname N_{\mathbb Q(h)/\mathbb Q}(a+bh)=a^4+b^4.
}
$$

### The same cyclotomic ring and Gaussian subring

The new unit is another primitive eighth root of unity:

$$
h=\zeta_8^3.
$$

Since $h=r^3$ and $r=h^3$, both units generate the same cyclotomic ring:

$$
\boxed{
\mathbb Z[h]
=\mathbb Z[r]
=\mathbb Z[\zeta_8].
}
$$

Squaring $h$ produces $-i$, which generates the same Gaussian ring as $i$:

$$
\boxed{
\mathbb Z[h^2]
=\mathbb Z[-i]
=\mathbb Z[i].
}
$$

Thus $r=\zeta_8$ and $h=\zeta_8^3$ are different generators of the same eighth-cyclotomic extension. Their squares select $i$ and $-i$, respectively, but both return to the same Gaussian subring.

## 17. The unit that separates the modulo-$4$ prime branches

The value that separates primes congruent to $1\pmod4$ from primes congruent to $3\pmod4$ is the ordinary Gaussian unit

$$
\boxed{h=\mathbin{\pm}i,\qquad h^2=-1.}
$$

This produces the exact branch behavior

$$
\boxed{
\begin{array}{c|c}
p\bmod4&\text{Behavior in }\mathbb Z[h]=\mathbb Z[i]\\ \hline
1&p\text{ splits into conjugate Gaussian factors}\\
3&p\text{ remains Gaussian prime}
\end{array}}
$$

For an odd prime $p$,

$$
\boxed{
p\equiv1\pmod4
\iff
p=a^2+b^2
\iff
p=(a+bi)(a-bi).
}
$$

In contrast,

$$
\boxed{
p\equiv3\pmod4
\Longrightarrow
p\neq a^2+b^2,
}
$$

and $p$ does not split in $\mathbb Z[i]$.

### Why $h^2=-1$ gives this separation

The conjugate product is

$$
(a+bh)(a-bh)=a^2-b^2h^2.
$$

Setting $h^2=-1$ gives the positive Gaussian norm

$$
\boxed{(a+bi)(a-bi)=a^2+b^2.}
$$

Every square is $0$ or $1\pmod4$. An odd sum of two squares must therefore have one even coordinate and one odd coordinate, giving

$$
0+1\equiv1\pmod4.
$$

It can never be congruent to $3\pmod4$. This modular obstruction creates the two branches.

### The modular square-root criterion

The same separation appears in the congruence

$$
x^2\equiv-1\pmod p.
$$

For an odd prime $p$,

$$
\boxed{
x^2\equiv-1\pmod p
\text{ has a solution}
\iff
p\equiv1\pmod4.
}
$$

For example, modulo $5$,

$$
2^2=4\equiv-1\pmod5,
$$

and $5$ splits as

$$
5=(2+i)(2-i).
$$

Modulo $13$,

$$
5^2=25\equiv-1\pmod{13},
$$

and

$$
13=(3+2i)(3-2i).
$$

Modulo $7$, no integer satisfies

$$
x^2\equiv-1\pmod7,
$$

and $7$ remains Gaussian prime.

The criterion can be expressed compactly using the Legendre symbol:

$$
\boxed{
\left(\frac{-1}{p}\right)
=(-1)^{(p-1)/2}
=
\begin{cases}
+1,&p\equiv1\pmod4,\\
-1,&p\equiv3\pmod4.
\end{cases}}
$$

### Relation to the eighth-cyclotomic generator

Let

$$
r=\frac{1+i}{\sqrt2}=\zeta_8.
$$

The separating Gaussian unit is obtained by squaring:

$$
\boxed{r^2=i.}
$$

The other choice is

$$
\boxed{r^6=-i,}
$$

which generates the same Gaussian ring:

$$
\mathbb Z[i]=\mathbb Z[-i].
$$

Thus, among powers of $r$, the values $r^2=i$ and $r^6=-i$ directly produce the modulo-$4$ splitting test. The odd powers $r,r^3,r^5,r^7$ generate the larger eighth-cyclotomic ring, whose full algebraic norm does not directly provide the same binary sum-of-two-squares separator.

The role of $h=\pm i$ is therefore not to represent both branches as sums of two squares. Its role is to distinguish them exactly:

$$
\boxed{
\begin{aligned}
p\equiv1\pmod4&\Longrightarrow p\text{ splits in }\mathbb Z[i],\\
p\equiv3\pmod4&\Longrightarrow p\text{ remains unsplit in }\mathbb Z[i].
\end{aligned}}
$$

## 18. Combining separation with universal representation

No single ordinary complex value $h$, equipped with one quadratic conjugate norm, can perform both of the following jobs simultaneously:

1. separate the $1\pmod4$ and $3\pmod4$ prime branches through Gaussian splitting;
2. represent every odd prime by that same conjugate norm.

The requirements conflict. Exact Gaussian separation uses

$$
h^2=-1,
$$

which gives

$$
(a+bh)(a-bh)=a^2+b^2
$$

and deliberately excludes primes congruent to $3\pmod4$. Universal representation of odd integers as differences of squares uses a split-complex unit

$$
j^2=1,
$$

which gives

$$
(A+Bj)(A-Bj)=A^2-B^2
$$

but no longer distinguishes the two modulo-$4$ branches.

### A paired two-channel construction

The two operations can be retained in separate components of the direct-product algebra

$$
\mathbb Z[i]\times\mathbb Z[j].
$$

Define the paired unit

$$
\boxed{H=(i,j)}.
$$

Then

$$
\boxed{H^2=(-1,1)}.
$$

The two coordinate projections are

$$
\pi_G(H)=i
$$

and

$$
\pi_S(H)=j.
$$

The Gaussian component $\pi_G$ supplies separation, while the split-complex component $\pi_S$ supplies a universal odd representation.

### Gaussian channel: branch separation

The Gaussian component uses

$$
(a+bi)(a-bi)=a^2+b^2.
$$

For odd primes,

$$
\boxed{
\begin{aligned}
p\equiv1\pmod4
&\Longrightarrow p\text{ splits in }\mathbb Z[i],\\
p\equiv3\pmod4
&\Longrightarrow p\text{ remains unsplit in }\mathbb Z[i].
\end{aligned}}
$$

This channel detects the prime branch but cannot express a $3\pmod4$ prime as a Gaussian conjugate norm.

### Split-complex channel: universal odd representation

For every odd positive integer $p$, define

$$
A=\frac{p+1}{2},
\qquad
B=\frac{p-1}{2}.
$$

Then

$$
A^2-B^2=p,
$$

and therefore

$$
\boxed{p=(A+Bj)(A-Bj).}
$$

This channel represents both modulo-$4$ branches, but the representation alone does not determine whether $p$ is prime or which branch contains it.

For $p=5$, the Gaussian channel gives

$$
5=(2+i)(2-i),
$$

while the split-complex channel gives

$$
5=(3+2j)(3-2j).
$$

The first channel identifies $5$ as a splitting prime.

For $p=7$, the Gaussian channel leaves $7$ unsplit, while the split-complex channel gives

$$
7=(4+3j)(4-3j).
$$

The two-channel behavior can be summarized as follows:

| $p\bmod4$ | Gaussian channel $\mathbb Z[i]$ | Split-complex channel $\mathbb Z[j]$ |
|---:|:---|:---|
| $1$ | Splits as $a^2+b^2$ | Represented as $A^2-B^2$ |
| $3$ | Remains unsplit | Represented as $A^2-B^2$ |

Thus,

$$
\boxed{
\text{Gaussian component}=\text{separator},
\qquad
\text{split-complex component}=\text{universal odd representation}.
}
$$

The paired object $H=(i,j)$ is not one ordinary complex scalar. It is one element of a product algebra whose two projections deliberately preserve two different norm behaviors.

### If every representation must use positive squares

The split-complex channel uses a difference of squares. If the representation must instead be a positive sum of squares, two Euclidean coordinates are insufficient for all $3\pmod4$ primes.

Quaternion norms provide the universal positive representation

$$
\operatorname N(a+bi+cj+dk)=a^2+b^2+c^2+d^2.
$$

By Lagrange's four-square theorem, every nonnegative integer has such a representation. However, the quaternion norm alone does not preserve the Gaussian split/unsplit distinction. The corresponding combined framework is therefore

$$
\boxed{
\mathbb Z[i]\text{ for modulo-}4\text{ separation}
\quad+\quad
\mathbb H\text{ for universal positive-square representation}.
}
$$

Consequently, one quadratic complex scalar cannot do both jobs with one norm, but a paired algebra or a separator-plus-quaternion framework can preserve both capabilities.

## 19. Summary

- The factor $1+i$ represents the prime $2$ geometrically through $2=-i(1+i)^2$.
- The factor $1+i$ also converts equal-parity Gaussian coordinates into integer coordinates under a $45^\circ$ rotation.
- Every even integer is a sum of two odd integers, but not necessarily a sum of two odd squares or two odd primes.
- Every odd integer is a difference of two consecutive squares.
- A Gaussian conjugate product represents a sum, not a difference: $(a+bi)(a-bi)=a^2+b^2$.
- No integer congruent to $3\pmod4$ is a sum of two squares.
- An integer congruent to $1\pmod4$ may be a sum of two squares, subject to the prime-factor criterion.
- Every prime congruent to $1\pmod4$ is a sum of two squares and splits in $\mathbb Z[i]$.
- Every prime congruent to $3\pmod4$ remains prime in $\mathbb Z[i]$.
- Both odd-prime residue branches participate in Goldbach decompositions: the $1\pmod4$ branch gives sums of squares, while the $3\pmod4$ branch can be translated using differences of consecutive squares.
- A four-square or signed-four-square branch formula reduces to two squares precisely when the final $X$ satisfies the sum-of-two-squares prime-exponent criterion.
- Gaussian factorization adds modular, parity, norm, and coordinate constraints to Goldbach decompositions without proving the existence of the required prime pair.
- Modulo $8$ refines the $1\pmod4$ branch into $1,5\pmod8$ and the $3\pmod4$ branch into $3,7\pmod8$, without changing which primes split in $\mathbb Z[i]$.
- Split-complex numbers encode differences of squares, while quaternion norms provide four positive orthogonal squares and represent every nonnegative integer.
- Gaussian integers detect sums of two squares and distinguish prime branches, whereas split-complex integers represent both odd branches uniformly as differences of consecutive squares.
- The scaled imaginary unit $h_0=i/\sqrt2$, rescaled integrally to $v^2=-2$, produces the norm $a^2+2c^2$ and represents exactly the odd-prime branches $1,3\pmod8$.
- The square root $h=(1+i)/\sqrt2$ of $i$ is a pure $45^\circ$ rotation; its eighth-cyclotomic algebraic norm sends $a+bh$ to $a^4+b^4$.
- Squaring the eighth-cyclotomic generator $r=\zeta_8$ gives $r^2=i$; restricting to even powers extracts the Gaussian subring $\mathbb Z[i]=\mathbb Z[r^2]$.
- The alternative generator $h=\zeta_8^3$ rotates by $135^\circ$, generates the same cyclotomic ring, and satisfies $\mathbb Z[h^2]=\mathbb Z[-i]=\mathbb Z[i]$.
- The choice $h=\pm i$, equivalently $h^2=-1$, is the exact modulo-$4$ separator: primes $1\pmod4$ split and primes $3\pmod4$ remain Gaussian prime.
- Separation and universal representation require distinct norm channels: $\mathbb Z[i]$ separates the branches, while $\mathbb Z[j]$ represents every odd integer by a difference of squares or $\mathbb H$ represents every nonnegative integer by four positive squares.

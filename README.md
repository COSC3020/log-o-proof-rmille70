[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/fbkbKZ5N)
# Asymptotic Equivalences

In the lectures, we said that logarithms with different bases don't affect the
asymptotic complexity of an algorithm. Prove that $O(\log_{2} n)$ is the same as
$O(\log_{5} n)$. Use the mathematical definition of $O$ -- do a formal proof,
not just the intuition.

I have started with the formal definition of $O$ below. Add your answer to this
markdown file. [This
page](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/writing-mathematical-expressions)
might help with the notation for mathematical expressions.

$T(n) \in O(f(n)) \iff \exists c, n_0: T(n) \leq c \cdot f(n) \forall n \geq n_0$

$O(\log_{2} n) = \exists c, n_0: T(n) \le c\log_{2}(n) \forall n \ge n_0$  {big-oh where $f(n) = \log_{2}(n)$}
$= \exists c, n_0: T(n) \le c\frac{\log(n)}{\log(2)} \forall n \ge n_0$    {by properties of logarithms}
$= \exists c, n_0: T(n) \le \frac{c\log(n)}{\log(2)} \forall n \ge n_0$    {multiply c into fraction}
$= \exists c, n_0: T(n) \le \log(n) \frac{c}{\log(2)} \forall n \ge n_0$   {factor out $\log(n)$ }
$O(\log_{5} n) = \exists c, n_0: T(n) \le c\log_{5}(n) \forall n \ge n_0$  {big-oh where $f(n) = \log_{5}(n)$}
$= \exists c, n_0: T(n) \le c\frac{\log(n)}{\log(5)} \forall n \ge n_0$    {by properties of logarithms}
$= \exists c, n_0: T(n) \le \frac{c\log(n)}{\log(5)} \forall n \ge n_0$    {multiply c into fraction}
$= \exists c, n_0: T(n) \le \log(n) \frac{c}{\log(5)} \forall n \ge n_0$   {factor out $\log(n)$ }

Since $c$ is just a constant, $c$ multiplied by a constant is still a constant. So $\frac{c}{\log(2)}$ and $\frac{c}{\log(5)}$ are both also constants. Thus $O(\log_{2} n)$ is logically equivilant $O(\log_{5} n)$ Q.E.D.
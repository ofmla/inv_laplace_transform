# inv_laplace_transform
Gaver Stehfest for numerically inverting the Laplace transform

### Description

Fortran implementation of the Gaver Stehfest algorithm, which was originally developed in 1970. Since its inception, this algorithm has gained widespread popularity for its ability to 
efficiently perform inverse Laplace transforms and ease of implementation.
[Stehfest, Harald. "Algorithm 368: Numerical inversion of Laplace transforms [D5]." Communications of the ACM 13.1 (1970): 47-49.](https://dl.acm.org/doi/pdf/10.1145/361953.361969)

The provided program applies this algorithm to determine the inverse Laplace transforms of the function $1/(s+1)$, whose result is $e^{(-t)}$. Inverse Laplace transforms of other analytic functions can be easily computed.

### Compiling

A [Fortran Package Manager](https://github.com/fortran-lang/fpm) (FPM) manifest file is included so that a simple program can be compiled with FPM. When you run the command:

```
fpm run --target gs-prog --profile release --V
```
you will get an ASCII datafile in multicolumn format. You can produce a plot giving the ASCII file as standard input to gnuplot.
```
plot 'fort.10' u 1: 2 w l, 'fort.10' u 1:3 w lp
```


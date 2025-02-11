# Recurrent Recurrences

Give big $\Theta$ bounds for the following recurrence relations.

1.
$$ T(n) =
    \begin{cases}
        1 & n \leq 1\\
        T\left(\frac{n}{13}\right) + 5 & n > 1
    \end{cases}
$$

2.
$$ T(n) =
    \begin{cases}
        1 & n \leq 1\\
        13 T\left(\frac{n}{13}\right) + 5 & n > 1
    \end{cases}
$$

3.
$$ T(n) =
    \begin{cases}
        1 & n \leq 1\\
        13 T\left(\frac{n}{13}\right) + 2n & n > 1
    \end{cases}
$$

## Answers
### Question 1
$T(n) = T(\frac{n}{13})+5$

$T(n) = (T(\frac{n}{13^2})+5)+5$

$T(n) = T(\frac{n}{13^2})+10$

$T(n) = T(\frac{n}{13^3})+15$

$T(n) = ...$

$T(n) = T(\frac{n}{13^i})+i \cdot 5$

For $i=log_{13}n$:

$T(n) = T(\frac{n}{13^log_{13}n})+log_{13}n \cdot 5$

$T(n) = T(1)+5 \cdot log_{13}n$

$T(n) = 1 + 5 \cdot log_{13} \in \Theta(log(n))$

Recurrence relation 1 has a bound of $\Theta(log(n))$



### Question 2
$T(n) = 13T(\frac{n}{13})+5$

$T(n) = 13(13T(\frac{n}{13^2})+5)+5$

$T(n) = 13^2 \cdot T(\frac{n}{13^2})+10$

$T(n) = 13^3 \cdot T(\frac{n}{13^3})+15$

$T(n) = ...$

$T(n) = 13^i \cdot T(\frac{n}{13^i})+i \cdot 5$

For $i=log_{13}n$:

$T(n) = 13^{log_{13}n} \cdot T(\frac{n}{13^log_{13}n})+log_{13}n \cdot 5$

$T(n) = n \cdot T(1)+5 \cdot log_{13}n$

$T(n) = n + 5 \cdot log_{13} \in \Theta(n)$

Recurrence relation 2 has a bound of $\Theta(n)$



### Question 3
$T(n) = 13T(\frac{n}{13})+2n$

$T(n) = 13(13T(\frac{n}{13^2})+\frac{2n}{13})+2n$

$T(n) = 13^2 \cdot T(\frac{n}{13^2})+4n$

$T(n) = 13^3 \cdot T(\frac{n}{13^3})+6n$

$T(n) = ...$

$T(n) = 13^i \cdot T(\frac{n}{13^i})+i \cdot 2n$

For $i=log_{13}n$:

$T(n) = 13^{log_{13}n} \cdot T(\frac{n}{13^log_{13}n})+log_{13}n \cdot 2n$

$T(n) = n \cdot T(1)+2n \cdot log_{13}n$

$T(n) = n + 2n \cdot log_{13} \in \Theta(n \cdot log(n))$

Recurrence relation 3 has a bound of $\Theta(n \cdot log(n))$



## Sources
I certify that I have listed all sources used to complete this exercise, including the use of any Large Language Models. All of the work is my own, except where stated otherwise. I am aware that plagiarism carries severe penalties and that if plagiarism is suspected, charges may be filed against me without prior notice.
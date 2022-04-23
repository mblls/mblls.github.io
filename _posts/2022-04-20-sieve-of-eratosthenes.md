---
title: How to Apply the Sieve of Eratosthenes
layout: post
---

* TOC
{:toc}

## Introduction

While working through math and competitive programming problems like those listed on Project Euler, inevitably you’re going to have to solve problems involving prime numbers (and as would be expected!). One type of prime number problem specifically deals in trying to all find prime numbers within a certain range. As an example, [Problem 3](https://projecteuler.net/problem=3) on Project Euler asks us to find the largest prime that is less than <kbd>600851475143</kbd>, which can be thought of as finding the last prime within the range $$[0:600851475143]$$.  

## Naive Algorithm

We can start solving this problem by using the naive algorithm for finding all primes within a bounded range as follows:

```
# Naive Algorithm.
n = 600851475143
primes_under_n = set()
for each number i in range(0:n):
  i_is_prime = True
  for each number j in range(0:i):
    if i%j == 0:
      i_is_prime = False
  if i_is_prime:
    primes_under_n.add(i)
```

This algorithm runs in <kbd>O(n^2)</kbd> time, where we are evaluating every number <kbd>i</kbd> within <kbd>[0:n]</kbd>, and then checking every number <kbd>j</kbd> within <kbd>[1:i]</kbd> to determine if <kbd>i</kbd> can be divided by <kbd>j</kbd> with no remainder (thus proving or disproving that the number is, in fact, prime). Since Problem 3 requires finding all primes up to 600851475143, this would be on the order of $$3*10^{19}$$ ($$~600851475143^{2}$$) total operations if you started from 0 and worked your way up to 600851475143.

If we assume for the sake of simplicity that modular division takes 1 clock cycle and we’re running this on a 1GHz processor, this algorithm will take 36000000000 seconds to complete.

$$(\frac{3*10^{19} operations}{1GHz per second} =  36000000000 seconds)$$

This means <mark>the naive algorithm would take ~1100 years to calculate in the worst case</mark>. Obviously we can do much better.

## Initial Optimizations

One very quick optimization we can make for specifically Problem 3 that the diligent reader probably noticed is to just start from n and work down in order to find the _largest_ prime. This will run on the order of <kbd>O(minutes)</kbd> on a Macbook Pro. Though this is better, it's only by a constant factor; our naive algorithm has not fundamentally changed.  

If we analyze the naive approach for bottlenecks we notice that the algorithm always evaluates all numbers up to <kbd>n</kbd>, including numbers that are very obviously not prime, such as even even numbers. What if we were to just check that whatever number <kbd>i</kbd> that we're evaluating the primality of isn't even first (where $$i \% 2 != 0$$)? We could effectively halve our problem space!

Staying with line of thinking... what about if we repeated that process on _all_ obviously not prime numbers? Notice that our naive algorithm will evaluate numbers that are multiples of numbers that we’ve already determined to _not_ be prime. What if we just didn't evaluate numbers that we know are multiples of other not prime numbers?

## Sieve of Eratosthenes

{% include image.html url="/assets/blog_1_primes/Sieve_of_Eratosthenes_animation.gif" description="Fig 2. Sieve of Eratosthenes [SK22]" %}

This approach is known as <mark>the Sieve of Eratosthenes (SoE). The SoE algorithm works by checking that the number you’re currently on isn’t a multiple of a number that we’ve previously determined to not be prime.</mark> We can picture the numbers <kbd>[1:n]</kbd> as a large grid of numbers (Fig. 1). For each number starting from 2 (1 is already known to be prime), we remove all numbers that are multiples of 2 from the grid. Now the next non crossed-out number is 3, so we cross out all numbers that are multiples of 3. Next non crossed-out number is 5. By repeating this, the next non-crossed out number is guaranteed to be a prime number. This process of elimination takes our time complexity from $$O(n^2)$$ to $$O(nlog(log(n))$$ (Fig. 2). You can find the full asymptotic derivation [here]( https://cp-algorithms.com/algebra/sieve-of-eratosthenes.html). This reduces our total number of computations from $$3*10^{19}$$ to 643571916360, a 4661480000% reduction in number of operations.

{% include image.html url="/assets/blog_1_primes/n^2 vs n_log(log(n)) vs n.png" description="Fig 1. n^2 vs. nlog(log(n))" %}

For the sake of solving similar range-based prime number problems on Project Euler, this algorithm vastly more than efficient. There are some subtle improvements that can be made to reduce the number of operations, which you can read about here [https://cp-algorithms.com/algebra/sieve-of-eratosthenes.html](https://cp-algorithms.com/algebra/sieve-of-eratosthenes.html) [JK14]. I encourage you to test out the SoE’s performance on your own machine, and try comparing its time-to-completion against the same algorithm with improvements made.

## References

- [JK14] "Sieve of Eratosthenes" by Jakob Kogler _et. all_ 2014 can be read here: [https://cp-algorithms.com/algebra/sieve-of-eratosthenes.html](https://cp-algorithms.com/algebra/sieve-of-eratosthenes.html) _Open source site dedicated to competitive programming algorithms and techniques._
- [W22] "Sieve of Eratosthenes" [https://en.wikipedia.org/wiki/Sieve_of_Eratosthenes](https://en.wikipedia.org/wiki/Sieve_of_Eratosthenes)
- [SK22] SKopp at German Wikipedia - Own work, Original image at [Image:Animation_Sieve_of_Eratosth.gif](https://commons.wikimedia.org/w/index.php?curid=2810935), CC BY-SA 3.0, [https://commons.wikimedia.org/w/index.php?curid=2810935](https://commons.wikimedia.org/w/index.php?curid=2810935)

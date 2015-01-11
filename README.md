# ErrorFreeTransforms

[![Build Status](https://travis-ci.org/dsiem/ErrorFreeTransforms.jl.svg?branch=master)](https://travis-ci.org/dsiem/ErrorFreeTransforms.jl)

Rounding errors are a common problem in floating point arithmetic. For a pair of
floating point numbers `a`, `b`, an error-free transformations `f` (EFT) is an
operation that maps `(a, b)` into `(x, y)`, where `a ○ b = x + y` and `x = fl(a
○ b)` with `○` being either addition, subtraction or multiplication. Standard
EFTs are the `TwoSum` algorithm by Knuth (implemented as `err_add`) and the
`TwoProd` algorithm by Dekker (implemented as `err_mul`).

This package implements several EFT from the scientific literature.

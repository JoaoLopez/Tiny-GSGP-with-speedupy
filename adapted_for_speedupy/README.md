# Tiny GSGP Experiment

## Experiment dependencies
This experiment has no dependencies.

To run the experiment, make sure you have the appropriate release of SpeeduPy installed. Instructions on which release to use and how to install it can be found [here](https://github.com/dew-uff/memoization/blob/main/README.md#reproducing-the-article-analyses). Ensure that the **speedupy/** folder is located in the same directory as the main experiment script.

## Trials Used in the Article
The five trials used on the memoization techniques article are:

- TINY_GSGP_10.py
- TINY_GSGP_20.py
- TINY_GSGP_40.py
- TINY_GSGP_50.py
- TINY_GSGP.py

To execute a trial, type:

```bash
python speedupy/setup_exp/setup.py SCRIPT_NAME.py
python SCRIPT_NAME.py --exec-mode manual
```

---
README.md content from the original repository:


TINY_GSGP.py: 
=============

A Tiny and Efficient Implementation of Geometric Semantic Genetic Programming Using Higher-Order Functions and Memoization

Author: Alberto Moraglio (albmor@gmail.com) 

Features:

- Individuals are represented directly as Python (anonymous) functions.

- Crossover and mutation are higher-order functions.

- Offspring functions call parent functions rather than embed their definitions (no grwoth, implicit ancestry trace).

- Memoization of individuals turns time complexity of fitness evalutation from exponential to constant.

- The final solution is a compiled function. It can be extracted using the ancestry trace to reconstruct its 'source code'. 

This implementation is to evolve Boolean expressions. It can be easily adapted to evolve arithmetic expressions or classifiers.

TINY_GSGP.nb: 
=============

A Tiny Implementation of Geometric Semantic Genetic Programming in Mathematica Using Algebraic Simplification.

Author: Alberto Moraglio (albmor@gmail.com)

This is a reimplementation of TINY_GSGP.py in Mathematica to compare the effect of simplification of offsrping. 

Features:

- Individuals are represented using symbolic expressions (Boolean expressions).

- Uniform initialisation/generation of random expressions.

- Crossover and mutation embed parent expressions in the offspring expression.

- Algebraic simplification of offspring prevents exponential growth.

- The final solution is short and understandable (no black-box).

TINY_GSHCGP.py: 
===============

An Implementation of Geometric Semantic *Hill Climber* Genetic Programming Using Higher-Order Functions and Memoization

Author: Alberto Moraglio (albmor@gmail.com)

Features:

- Same as TINY_GSGP.py, substituting the evolutionary algorithm with a hill-climber.

- The fitness landscape seen by Geometric Semantic operators is always unimodal. A hill climber can reach the optimum.

- Offspring functions call parent functions rather than embed their definitions (no grwoth, implicit ancestry trace).

- Even if offspring functions embedded parent function definition, the growth is linear in the number of generation (not exponential as with crossover). 

- Memoization of individuals turns time complexity of fitness evalutation from linear to constant (not exponential to constant as with crossover).

- Implicit ancestry trace and memoization not strictly necessary with hill-climber for efficent implementation.

- The final solution is a compiled function. It can be extracted using the ancestry trace to reconstruct its 'source code'. 

This implementation is to evolve Boolean expressions. It can be easily adapted to evolve arithmetic expressions or classifiers.

TINY_GSHCGP.nb:
===============

An Implementation of Geometric Semantic *Hill Climber* Genetic Programming in Mathematica Using Algebraic Simplification.

Author: Alberto Moraglio (albmor@gmail.com)

Features:

- The fitness landscape seen by Geometric Semantic operators is always unimodal. A hill-climber can reach the optimum.

- Mutation embeds parent expression in the offspring expression.

- Algebraic simplification of offspring.

- Offspring size growth without simplification is linear in the number of generation (simplification is not strictly needed for space efficiency).

- Final solution short and understandable.

TINY_GSHCGP _ARIT.nb: 
=====================

Geometric Semantic Hill Climber Genetic Programming in Mathematica for *Arithmetic Expressions*.

Author: Alberto Moraglio (albmor@gmail.com)

Features:

- It searches the space of arithmentic expressions (polynomials or fractional polynomials if division is used).

- Fithess is based on a training set (not on all inputs as for Boolean expressions). 

- Algebraic simplification of offspring.

- Generalisation test (on unseen examples).

TINY_GSGP _ARIT.nb: 
===================

Geometric Semantic Genetic Programming in Mathematica for *Arithmetic Expressions*.

Author: Alberto Moraglio (albmor@gmail.com)

Features:

- It evolves arithmentic expressions (polynomials or fractional polynomials if division is used).

- Fithess is based on a training set (not on all inputs as for Boolean expressions).

- Algebraic simplification of offspring.

- Generalisation test (on unseen examples).
 


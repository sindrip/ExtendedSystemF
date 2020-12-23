# Bidirectional Damas-Milner Type Synthesis for Predicative System F

An implementation of the paper ["Complete and Easy Bidirectional Typechecking
for Higher-Rank Polymorphism"](https://dl.acm.org/doi/abs/10.1145/2544174.2500582) by Dunfield and Krishnaswami.

We implement the Full Damas-Milner inferrance as proposed in the paper, and identify that the single rule change is not enough. So in addition to changes to rule T-Abs-Synth, we also make similar changes to T-App-Elim that are not mentioned in the paper.

### Try it out

This package is developed with GHC 8.8.4, we reccomend [ghcup](https://www.haskell.org/ghcup/) if you do not have the toolchain installed.

To try out some of our examples, cd into the directory and launch ghci with the following command:
```
$ cabal repl
```

When you're in the repl, load in the Examples module and try calling synthType on some of them like one and succ(one) and compare the out.

```
λ :m +Examples
λ synthType one
...
λ synthType (App suc one)
...
```

 

# FP

## What are the Combinators?

%

The term combinator refers to the combinator pattern:

Usually there is some type T, some "primitive" values of type T, and some "combinators" which can combine values of type T in various ways to build up more complex values of type T.

The general form of a combinator is:

```
combinator: Thing -> Thing
```

## What is a Functor?

%

"An object that implements a map function which, while running over each value in the object to produce a new object, adheres to two rules:

Preserves identity

```
object.map(x => x) ≍ object
```

Composable

```
object.map(compose(f, g)) ≍ object.map(g).map(f)
```

(f, g are arbitrary functions)"
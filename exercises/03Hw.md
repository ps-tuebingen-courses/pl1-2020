# Homework 03

Put your Scala file(s) with the solutions in this repository.

Deadline: May 8, 2020, 10:00h

## Task 1: Visitors

Translate `countVisitor` and `printVisitor` from their definition for AE in the lecture
(see [`04-ae.scala`](https://github.com/ps-tuebingen-courses/pl1-2020/blob/master/lecturenotes/04-ae.scala#L147),
in object `Visitors`) to one using pattern matching.

Example: Translating the eval visitor from object `Visitors` in this way leads to
the `eval` method from [`03-desugaring.scala`](https://github.com/ps-tuebingen-courses/pl1-2020/blob/master/lecturenotes/03-desugaring.scala#L18) (in object `AE`).

## Task 2: Enhancing FAE with booleans

Add booleans, including a conditional statement (`If`), to FAE.

Hint: Start with the code from the lecture (see [`07-fae.scala`](https://github.com/ps-tuebingen-courses/pl1-2020/blob/master/lecturenotes/07-fae.scala)).
Use a case class analogous to `Num`.

Example: `If(Bool(true), Num(4), Num(2))` should evaluate to `4` and `If(Bool(false), Num(4), Num(2))` should evaluate to `2`.

Questions for you:

1. I left some freedom of design in the desired behavior of `If`. Can you identify the two different behaviors (which do not differ in the evaluation result)? Note: One of them is certainly more prevalent in existing PL.
2. Are there any features you would want to add to make this language with booleans more useful?

## Task 3: Closures

Change the *environment-based* FAE interpreter from the lecture to only close
over free variables.

Hint: The FAE interpreter from the lecture always puts
the whole environment in the closure, but it would be enough
to store the bindings for all free variables of the function.

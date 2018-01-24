# CS43 Functional Programming in Clojure: Assignment 1

## Problem 1:

Write a function which calculates the least common multiple. 
Your function should accept a variable number of positive 
integers or ratios.

`(lcm 5 3 7) = 105`

`(lcm 3/4 1/6) = 3/2`

## Problem 2:

Write a function that returns a lazy sequence of the Catalan numbers (https://en.wikipedia.org/wiki/Catalan_number).

Use the recurrence relation

![recurrence](https://wikimedia.org/api/rest_v1/media/math/render/svg/2b880e7e47a753e31ff455ad0d292746f9611f97)

`(take 5 (catalan)) = (1 1 2 5 14)`

## Problem 3:

Write a function to determine the best poker hand that can 
be made with five cards. The hand rankings are listed below 
for your convenience:

- Straight flush: All cards in the same suit, and in sequence
- Four of a kind: Four of the cards have the same rank
- Full House: Three cards of one rank, the other two of another rank
- Flush: All cards in the same suit
- Straight: All cards in sequence (aces can be high or low, but not both at once)
- Three of a kind: Three of the cards have the same rank
- Two pair: Two pairs of cards have the same rank
- Pair: Two cards have the same rank
- High card: None of the above conditions are met"

`(best-poker-hand ["HA" "DA" "HQ" "SQ" "HT"]) = :two-pair`

`(best-poker-hand ["HA" "HK" "HQ" "HJ" "HT"]) = :straight-flush`

`(best-poker-hand ["HA" "D2" "H3" "C9" "DJ"]) = :high-card`

## Problem 4:

The comp function in clojure.core takes in a set of functions and returns a function that is a composition of those functions. More formally, applying comp on the functions f1, f2, ..., fn creates a new function g such that

`g(x1, x2, ..., xn) = f1(f2(...(fn(x1, x2, ..., xn))))`

Implement your own version of the comp function.

## Problem 5 (Extra credit):

Clone our implementation of Hearts from https://github.com/jiangts/hearts-clojure.  Follow the instructions in the repo to run the code.

Interact with the application in the REPL to understand what each function does.  Explore the codebase and implement your own versions of any functions you find interesting.

# DFA-Minimization
## Finite Automata:
Finite Automata (FA) is the simplest machine to recognize patterns. The finite automata or finite 
state machine is an abstract machine that has five elements or tuples. It has a set of states and rules 
for moving from one state to another but it depends upon the applied input symbol. Basically, it is 
an abstract model of a digital computer 
DFAs, also known as deterministic finite automata, are finite state machines that accept or reject 
character strings by parsing them through a sequence that is specific to each string. It is said to be 
"deterministic" when each string, and thus each state sequence, is distinct. A DFA parses a string 
of symbols through DFA automata, and each input symbol advances to the next possible state.
Because there are only a finite number of states that these machines can achieve, they are given the 
name finite. Only if a finite automaton can meet both requirements is it referred to as deterministic. 
DFAs are different from non-deterministic automata in that the latter can switch between numerous 
states and be active in several states simultaneously.
Minimization of DFA: 
DFA minimization stands for converting a given DFA to its equivalent DFA with minimum 
number of states. DFA minimization is also called as Optimization of DFA.
The DFA in its minimal form is called as a Minimal DFA.
The two popular methods for minimizing a DFA are –
i. Equivalence Method
ii. Myhill Nerode Theorem

Steps –
1. Create the pairs of all the states involved in DFA.
2. Mark all the pairs (Qa,Qb) such a that Qa is Final state and Qb is Non-Final State.
3. If there is any unmarked pair (Qa,Qb) such a that δ(Qa,x) and δ(Qb,x) is marked, then mark 
(Qa,Qb). 
Here x is a input symbol. Repeat this step until no more marking can be made.
We have checked for all the unmarked pairs but don’t need to stop here we need to continue this 
process until no more markings can be made.
4. Combine all the unmarked pairs and make them as a single state in the minimized DFA.



## Overview
This project implements the DFA minimization algorithm, which is used to reduce the number of states in a deterministic finite automaton (DFA) while preserving its behavior. DFA minimization is crucial for simplifying DFA representations and optimizing their performance.

The implementation is done in Python, providing a straightforward demonstration of how DFA minimization works.

## Features
- Accepts DFA as input in a specified format.
- Applies the minimization algorithm to reduce the DFA's number of states.
- Generates a minimized DFA with equivalent behaviour to the original DFA.

## Example   
Consider the following DFA 

![Alt text](



# DFA-Minimization using Myhill Nerode Theorem

This project implements the DFA minimization algorithm, which is used to reduce the number of states in a deterministic finite automaton (DFA) while preserving its behavior. DFA minimization is crucial for simplifying DFA representations and optimizing their performance.

## Theory of Finite Automata

Finite Automata (FA) is the simplest machine to recognize patterns. The finite automata or finite state machine is an abstract machine that has five elements or tuples. It has a set of states and rules for moving from one state to another but it depends upon the applied input symbol. It is an abstract model of a digital computer DFAs, also known as deterministic finite automata, are finite state machines that accept or reject character strings by parsing them through a sequence that is specific to each string. It is said to be "deterministic" when each string, and thus each state sequence, is distinct.
DFAs are different from non-deterministic automata in that the latter can switch between numerous states and be active in several states simultaneously. Minimization of DFA: DFA minimization stands for converting a given DFA to its equivalent DFA with minimum number of states. DFA minimization is also called as Optimization of DFA. 

## Myhill Nerode Theorem 
Steps –
1. Create the pairs of all the states involved in DFA.
2. Mark all the pairs (Qa,Qb) such a that Qa is Final state and Qb is Non-Final State.
3. If there is any unmarked pair (Qa,Qb) such a that δ(Qa,x) and δ(Qb,x) is marked, then mark 
(Qa,Qb). 
Here x is a input symbol. Repeat this step until no more marking can be made.
We have checked for all the unmarked pairs but don’t need to stop here we need to continue this 
process until no more markings can be made.
4. Combine all the unmarked pairs and make them as a single state in the minimized DFA.


## Usage/Examples
Consider the following DFA 

![Alt text](Img/1.png)

Create the pairs of all the states involved in DFA and mark all the pairs (Qa,Qb) such a that Qa  is 
Final state and QB is Non-Final State. 

![Alt text](Img/2.png)

• Check for the unmarked pair Q2,Q1 <br>
• Check when x=0 : δ(Q2,0) = Q4 and δ(Q1,0) = Q3, check if the pair Q4,Q3 is marked and no it is not 
marked. <br>
• Check when x=1 : δ(Q2,1) = Q3 and δ(Q1,1) = Q4, check if the pair Q4,Q3 is marked and no it is not 
marked. <br>
• Hence we cannot mark the pair Q2,Q1. <br>
• Check for the unmarked pair Q3,Q0 <br>
• Check when x=0 : δ(Q3,0) = Q5 and δ(Q0,0) = Q1, check if the pair Q5,Q1 is marked and no it is not 
marked. <br>
• Check when x=1 : δ(Q3,1) = Q5 and δ(Q0,1) = Q2, check if the pair Q5,Q2 is marked and no it is not 
marked. <br>
• Hence we cannot mark the pair Q3,Q0. <br>
• Check for the unmarked pair Q4,Q0 <br>
• Check when x=0 : δ(Q4,0) = Q5 and δ(Q0,0) = Q1, check if the pair Q5,Q1 is marked and no it is not 
marked. <br>
• Check when x=1 : δ(Q4,1) = Q5 and δ(Q0,1) = Q2, check if the pair Q5,Q2 is marked and no it is not 
marked. <br>
• Hence we cannot mark the pair Q4,Q0. <br>
• Check for the unmarked pair Q4,Q3 <br>
• Check when x=0 : δ(Q4,0) = Q5 and δ(Q3,0) = Q5, Such pair of state Q5,Q5 don’t exists. <br>
• Check when x=1 : δ(Q4,1) = Q5 and δ(Q3,1) = Q5, Such pair of state Q5,Q5 don’t exists. <br>
• Hence we cannot mark the pair Q4,Q3. <br>
• Check for the unmarked pair Q5,Q1 <br>
• Check when x=0 : δ(Q5,0) = Q5 and δ(Q1,0) = Q3, check if the pair Q5,Q3 is marked and yes it is 
marked. <br>
• Hence we can mark the pair Q5,Q1. <br>
• Check for the unmarked pair Q5,Q2 <br>
• Check when x=0 : δ(Q5,0) = Q5 and δ(Q1,0) = Q4, check if the pair Q5,Q4 is marked and 
yes it is marked. <br>
• Hence we can mark the pair Q5,Q2. <br>

![Alt text](Img/3.png)

• We have checked for all the unmarked pairs but don’t need to stop here we need to continue this process until 
no more markings can be made. <br>
• Check for the unmarked pair Q2,Q1 <br> 
• Check when x=0 : δ(Q2,0) = Q4 and δ(Q1,0) = Q3, check if the pair Q4,Q3 is marked and no it is not 
marked. <br>
• Check when x=1 : δ(Q2,1) = Q3 and δ(Q1,1) = Q4, check if the pair Q4,Q3 is marked and no it is not 
marked. <br>
• Hence we cannot mark the pair Q2,Q1. <br>
• Check for the unmarked pair Q3,Q0 <br>
• Check when x=0 : δ(Q3,0) = Q5 and δ(Q0,0) = Q1, check if the pair Q5,Q1 is marked and yes it is 
marked. <br>
• Hence we can mark the pair Q3,Q0. <br>
• Check for the unmarked pair Q4,Q0 <br>
• Check when x=0 : δ(Q3,0) = Q5 and δ(Q0,0) = Q1, check if the pair Q5,Q1 is marked and 
yes it is marked. <br>
• Hence we can mark the pair Q4,Q0. <br>
Combine all the unmarked pairs and make them as a single state in the minimized DFA. <br>
• The unmarked Pairs are Q2,Q1 and Q4,Q3 hence we combine them. 
<br>
Following is the Minimized DFA with Q1Q2 and Q3Q4 as the combined states.

![Alt text](Img/4.png)

## Demo

Input 

![Alt text](Img/5.png)

Algorithm Implementation – (Note in the image given below for our algorithm we only consider 
the lower half matrix and 1 in the matrix denotes marked state and 0 unmarked states) <br>

![Alt text](Img/6.png)

Hence this is how we perform the minimization of the DFA using the Myhill Nerode Theorem 
or the Table filling method

![Alt text](Img/7.png)


## Programming Language and Library
- Python is the implementation language with libraries
  - Numpy
  - Pandas

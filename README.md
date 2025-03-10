# ND-Packing-Solver
Implementation of reducing N-Dimensional polyomino packing puzzles to the exact cover problem in python.

Inspired by [polyomino-solver](https://github.com/cemulate/polyomino-solver).  
Test puzzles from [puzzlewillbeplayed](https://puzzlewillbeplayed.com).  
Y25 info from [Herbert Kociemba](https://kociemba.org/themen/125puzzle/index.html#reference).  
Exact cover is solved via [xcover](https://github.com/johnrudge/xcover) python package.  

Note: Exact cover problems are NP-complete which means solve times can get very long very quickly as problems get larger.

## Why? 

I tried to solve the "25Y" or "125 cube" puzzle. The puzzle consists of 25 Y-shaped pentomino and the goal is to pack these pieces into a 5x5x5 box. (See images). Ended up with something more general.

Puzzle: 

![](https://github.com/xroi/ND-Packing-Solver/blob/main/assets/125puzBig.jpg)

I was able to find 60672 solutions (Which is apparently all of them) in 5 minutes CPU time. These are actually 60672/48=1264 solution if not counting symmetries. Finally I was able to solve this puzzle which laid shattered on my shelf for so long (in 1264 unique ways)!

![](https://github.com/xroi/ND-Packing-Solver/blob/main/assets/sol1.png)
![](https://github.com/xroi/ND-Packing-Solver/blob/main/assets/sol2.png)
![](https://github.com/xroi/ND-Packing-Solver/blob/main/assets/sol3.png)

## ND Packing

An example usage for packing N dimensions would be a job scheduler. One axis would be the expected execution time for the job, and the rest would be the system resources, i.e. RAM, CPUs, GPUs, etc. This is however a very inefficient way to implement a job scheduler due to the NP-completeness of the problem, plus by default the scheduler would be offline which is usually undesirable. 

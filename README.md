# ND-Packing-Solver
Implementation of reducing ND polymino packing puzzle to the exact cover problem in python.  

Inspired by [polyomino-solver](https://github.com/cemulate/polyomino-solver).  
Test puzzles from [puzzlewillbeplayed](https://puzzlewillbeplayed.com).  
Y25 info from [Herbert Kociemba](https://kociemba.org/themen/125puzzle/index.html#reference).  
Exact cover is solved via [xcover](https://github.com/johnrudge/xcover) python package.  

Note: Exact cover problems are NP-complete which means solve times can get very long very quickly as problems get larger.

## Why? 

I tried to solve the "25Y" or "125 cube" puzzle. The puzzle consists of 25 of the Y-shaped pentomino and the goal is to pack these pieces into a 5x5x5 box. (See images). Ended up with something more general. Finally I was able to solve this stupid puzzle which laid shattered on my shelf for so long!

Puzzle: 

![](https://github.com/xroi/ND-Packing-Solver/blob/master/assets/125puzBig.jpg)

Some solutions (I found 60672 solutions, or 1264 if not counting symmetries):

![](https://github.com/xroi/ND-Packing-Solver/blob/master/assets/sol1.png)
![](https://github.com/xroi/ND-Packing-Solver/blob/master/assets/sol2.png)
![](https://github.com/xroi/ND-Packing-Solver/blob/master/assets/sol3.png)

## >3D Packing

An example usage for packing N dimensions would be a job scheduler. One axis would be the expected execution time for the job, and the rest would be the system resources, i.e. RAM, CPUs, GPUs, etc. This is however a very inefficient way to implement a job scheduler due to the NP-completeness of the problem, plus by default the scheduler would be offline which is usually undesirable. 
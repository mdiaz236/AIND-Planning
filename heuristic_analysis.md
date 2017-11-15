# Heuristic Analysis

## Introduction
Using search.py, I ran the three air cargo problems for three non-heuristic search algorithms and astar with three heuristics.  The uninformed non-heuristic search algorithms are breadth first search, depth first graph search and uniform cost search.  The astart heuristics are  h1 (estimated cost is always 1), ignore preconditions, and planning graph level sum.

## Plan Length
All search approaches except for depth first graph were able to find optimal plans.  Figure 1 shows a comparison of the solution reached by each approach.  The plan for depth first seems to wander until it finds a solution and there are a repeated actions, which is unnecessary for this problem domain.  Figure 2 show the percentage of repeated actions for each solution.
![Figure 1](/Users/mdiaz/CompSci/AI/AIND/AIND-Planning/plan_length.png =600x240)
*Figure 1: Plan length comparison*

![Figure 2](/Users/mdiaz/CompSci/AI/AIND/AIND-Planning/repeated_action_pct.png =600x240)
*Figure 2: Percent of repeated actions (unique actions / total solution length)*

## New Nodes
Of the non-heuristic approaches, depth first graph search had the fewest number of new nodes.  Of the heuristic approaches, astar with level sum had the fewest.  Level sum also had the fewest over all with ignore preconditions (Problem 2) or depth first graph (Problems 1 and 3) having the second fewest. See Figure 3 for a chart of the number of new nodes.
![Figure 3](/Users/mdiaz/CompSci/AI/AIND/AIND-Planning/new_nodes.png =600x240)
*Figure 3: New nodes for search approaches and problems*

## Node Expansions
The number of node expansions had a order of results as the number of new nodes.  Astar had the fewest with ignore preconditions or depth first graph coming in second.  You can compare Figure 4 to Figure 3 to see that the shape of charts are similar.

![Figure 4](/Users/mdiaz/CompSci/AI/AIND/AIND-Planning/expansions.png =600x240)
*Figure 4: Nodes expanded for search approaches and problems*

## Goal Tests
Goal tests match new nodes and node expansions in the ordering of results and the shape of charts.  See Figure 5.
![Figure 5](/Users/mdiaz/CompSci/AI/AIND/AIND-Planning/goal_tests.png =600x240)
*Figure 5: Counts of goals tests*

## Elapsed Time
Depth first graph search had the shortest elapsed time for non heuristic approaches. This is due to the graph search coming across a non optimal solution directly  uniform cost search is the second quickest amongst non-heuristic approaches.

Astar ignore preconditions is the fastest of the heuristic approaches as well as fasted of all approaches except problem 1 (where depth first was faster). Although level sum did less expansion of nodes and goal tests, calculating the level cost is expensive.

![Figure 6](/Users/mdiaz/CompSci/AI/AIND/AIND-Planning/elapsed_time.png =600x240)
Figure 6: Elapsed time in seconds

## H1, Breadth First, Uniform Cost
Astar with the h1 heuristic, breadth first and uniform cost search approaches all have similar results for all metrics.  Their search approach is similar, with slight differences in how their computation.

## Conclusion
The fasted optimal approach is astar using the ignore preconditions heuristic.  Level sum is too expensive to calculate for this problem domain and depth first is non optimal.  Ignore preconditions is efficient to calculate and estimates the actual cost well enough.

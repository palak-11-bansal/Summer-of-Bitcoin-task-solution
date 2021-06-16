# Summer-of-Bitcoin-task-solution
# Description of files for this repo :
*  sb_README.pdf : Problem Statement
* solution.cpp : Source Code for the problem
* mempool.csv : Input Dataset for the mempool
* block.txt : output containing Block Transactions
# Understanding the Problem Statement :
1. Read a file mempool.csv, and make unordered map of txid , fee , weight , parent_txids
2. Make a fuction to check if the transaction is valid or not. It will be valid only if it's parent transactions have been included before.
3. We need to devise an alogrithm such that total fee of the block containing valid transactions is maximized given the constraint that total weight of the block does not exceed 4000000. 
# Approach used:
 This is basically a optimization problem which can be solved using Knapsack algorithm: greedy method.
* Select the transactions with highest value of fee/weight. The logic behind this is to minimize the leftover weight and maximize the fee.
* Check if the selected transaction is valid. That is all its parents are already included in the block.
* If the transaction is valid include the transaction and update fee and weight and erase it from curr set. If it is not valid go to next highest transaction.
# Output:
* total number of transactions: 5214
* number of transactions included in the valid block: 3174
* total fee: 5696031
* total weight: 3999936
### Happy Coding:)

 

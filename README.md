# Java Program to Implement an LRU Cache

## Problem Statement
Implement a basic version of a Least Recently Used (LRU) Cache with `get` and `put` operations.

## Approach
The LRU Cache is implemented using a doubly linked list and a hash map:
- The doubly linked list maintains the order of elements based on their usage.
- The hash map provides O(1) access to the nodes in the linked list.

## Code Explanation
- The `LRUCache` class contains a doubly linked list and a hash map.
- The `put` method inserts or updates a value and ensures the cache does not exceed its capacity.
- The `get` method retrieves a value and updates the usage order.
- The `remove` and `insert` helper methods manage the linked list operations.

## How to Run
1. Save the code in the `src` directory.
2. Open a terminal and navigate to the `LRUCacheProject` directory.
3. Compile the code using: `javac src/Main.java`
4. Run the compiled code using: `java -cp src Main`

## Test Cases
- Capacity: 2
  - `put(1, 1)`
  - `put(2, 2)`
  - `get(1)` -> returns 1
  - `put(3, 3)` -> evicts key 2
  - `get(2)` -> returns -1 (not found)
  - `put(4, 4)` -> evicts key 1
  - `get(1)` -> returns -1 (not found)
  - `get(3)` -> returns 3
  - `get(4)` -> returns 4

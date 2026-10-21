# The FAANG Pattern Sheet

**~150 hand-picked LeetCode problems, organized by pattern — not by topic, not by random order.**

> Interviews don't test 3000 problems. They test ~20 patterns. If you can recognize the pattern within 10 seconds of reading a problem, you've already done half the interview. This sheet gives you the patterns, the recognition triggers, and only the problems worth your time. No solutions here — this is the *map*, not the answers.

**Who this is for — everyone, via the Level Router below:**
- 🐣 You don't know what a loop is → start at **Level 0**
- 🌱 You know loops but freeze on LeetCode → **Level 1**
- 🎯 Interview in 4–10 weeks → **Level 2**
- 🏆 Already cleared FAANG, need revision → **Level 3**

**How this compares to the sheets you've heard of:**

| Sheet | Problems | Organized by | Gap this sheet fills |
|---|---|---|---|
| [Blind 75](https://www.techinterviewhandbook.org/best-practice-questions/) | 75 | Topic | No tiers, no beginner path, misses tries/intervals/greedy depth |
| [NeetCode 150](https://neetcode.io/practice) | 150 | Topic | Great, but flat difficulty inside each topic; no "revision-only" cut |
| [Grind 75](https://www.techinterviewhandbook.org/grind75/) | 75–169 | Week schedule | Schedule-first, not pattern-first |
| [Sean Prashad Patterns](https://seanprashad.com/leetcode-patterns/) | ~170 | Pattern | No learning path for beginners |
| **This sheet** | ~150 | **Pattern + tier + level** | One file, every level, trigger table, revision speedrun |

Full credit to those authors — this sheet is a curated union of their highest-signal problems plus known company-frequency classics.

---

## 🧭 Level Router — pick your entry point

### 🐣 Level 0 — "I don't know loops yet"

Do **not** touch the pattern sections yet. Spend ~2 weeks here:

1. Learn in this order: variables → `if/else` → loops (`for`, `while`) → functions → lists/arrays → strings. Any free source works (CS50, freeCodeCamp, or `PYTHON_BASICS.md` if you have this repo).
2. Then solve these 8 problems. They need only loops and `if`. The goal is NOT cleverness — it's building the habit of *reading a problem → writing code → submitting → fixing*:

| # | Problem | Why it's here |
|---|---|---|
| 1480 | [Running Sum of 1d Array](https://leetcode.com/problems/running-sum-of-1d-array/) | Your first loop over an array |
| 1929 | [Concatenation of Array](https://leetcode.com/problems/concatenation-of-array/) | Building a new array |
| 1672 | [Richest Customer Wealth](https://leetcode.com/problems/richest-customer-wealth/) | Nested loops |
| 412 | [Fizz Buzz](https://leetcode.com/problems/fizz-buzz/) | Loop + conditions |
| 344 | [Reverse String](https://leetcode.com/problems/reverse-string/) | Swapping with indices |
| 9 | [Palindrome Number](https://leetcode.com/problems/palindrome-number/) | Working with digits |
| 58 | [Length of Last Word](https://leetcode.com/problems/length-of-last-word/) | String walking |
| 27 | [Remove Element](https://leetcode.com/problems/remove-element/) | In-place array editing |

When these feel easy → you're Level 1. That's the whole gate.

### 🌱 Level 1 — "I know loops"

Go through the pattern sections **in order** (they're dependency-sorted — later patterns build on earlier ones). Solve only 🟢 **Warm-up** and 🔵 **Core** rows. Skip every 🔴 row — they exist for later you. Read the "What it is" blurb before attempting; if stuck 25 minutes, read any solution, then **redo it from a blank editor the next day**.

### 🎯 Level 2 — "Interview in 4–10 weeks"

All tiers, in order. Schedules:

- **4 weeks (emergency):** only ⭐ rows (~70 problems) — 2–3/day. This is the highest-frequency interview set.
- **8 weeks (standard):** patterns 1–10 in weeks 1–4, patterns 11–21 in weeks 5–7, week 8 = redo every ⭐ you got wrong.
- **12 weeks (thorough):** everything, ~2 problems/day, one full rest day/week, last 2 weeks = mock interviews + ⭐ redo.

### 🏆 Level 3 — "Cleared FAANG before, just revising"

You don't need volume, you need *recall*. Do exactly two things:

1. Read the **10-Second Trigger Table** below until every row is instant.
2. Speedrun the **⭐ rows only** (~70 problems). Rule: 5 minutes to state pattern + approach out loud. If you can, skip the code. If you can't, solve it fully.

---

## ⚡ The 10-Second Trigger Table

Memorize this. It's the sheet's core asset.

| The problem says / shows... | Pattern → section |
|---|---|
| "Find pair/duplicate/count occurrences", need O(1) lookup | Arrays & Hashing → §1 |
| Sorted array + find pair; compare from both ends; in-place shuffle | Two Pointers → §2 |
| "Longest/shortest/count **contiguous** subarray/substring with condition" | Sliding Window → §3 |
| "Subarray **sum** equals k", range-sum queries | Prefix Sum + HashMap → §4 |
| Matching brackets; undo/nesting; "next greater/smaller element"; histogram | Stack / Monotonic Stack → §5 |
| Sorted or rotated array; "O(log n)"; "minimum x such that condition holds" | Binary Search → §6 |
| Pointers/nodes; cycle; middle; reverse in place | Linked List → §7 |
| Tree + "level by level" | Tree BFS → §8 |
| Tree + path/depth/subtree property | Tree DFS → §8 |
| "Binary **search** tree", k-th smallest, validate ordering | BST → §9 |
| "Top K", "K closest", "K-th largest", "most frequent", median of stream | Heap → §10 |
| "Generate **all** combinations/permutations/subsets/boards" | Backtracking → §11 |
| Prefix matching, autocomplete, dictionary of words | Trie → §12 |
| Grid regions/islands; "shortest path" unweighted; spreading (rot/fire) | Graph BFS/DFS → §13 |
| Prerequisites, dependency order, "can you finish all courses" | Topological Sort → §14 |
| "Are these connected", merge groups/accounts | Union-Find → §15 |
| Overlapping intervals, meeting rooms, calendar | Intervals → §16 |
| Local choice is provably safe (jumps, gas, partitions) | Greedy → §17 |
| "How many ways", "max/min result of sequential choices", overlapping subproblems | 1-D DP → §18 |
| Grid paths; two strings compared; pick items under capacity | 2-D / Knapsack DP → §19 |
| XOR tricks, "appears once", bits, powers of two | Bit Manipulation → §20 |
| "Design a data structure with O(1) operations" | Design → §21 |

---

**How to read the tables below**
- 🟢 Warm-up (build confidence) · 🔵 Core (what interviews actually ask) · 🔴 FAANG (hard tier / senior loops)
- ⭐ = interview classic. Asked constantly. The Level-3 revision set = all ⭐ rows.
- Companies = well-known frequency data, approximate. 🔒 = LeetCode Premium problem (a free near-identical alternative is noted).
- If this repo's `DSA/` folder is available to you, each section's **Learn it** points at the matching solved-template file.

---

## §1 Arrays & Hashing

**What it is:** A hash map is a magic notebook — you write something down once and later ask "have I seen this?" in constant time. Most "find the duplicate / pair / count" problems stop being about searching and start being about *remembering*.
**Trigger:** counting, duplicates, "seen before", pair lookup, grouping.
**Learn it:** `DSA/01_arrays.py`, `DSA/04_hash_tables.py` · [NeetCode: Arrays & Hashing](https://neetcode.io/roadmap)

| Tier | # | Problem | Diff | Companies | ⭐ |
|---|---|---|---|---|---|
| 🟢 | 217 | [Contains Duplicate](https://leetcode.com/problems/contains-duplicate/) | E | Amazon, Apple | |
| 🟢 | 242 | [Valid Anagram](https://leetcode.com/problems/valid-anagram/) | E | Bloomberg, Amazon | |
| 🟢 | 1 | [Two Sum](https://leetcode.com/problems/two-sum/) | E | Everyone, always | ⭐ |
| 🔵 | 49 | [Group Anagrams](https://leetcode.com/problems/group-anagrams/) | M | Amazon, Meta | ⭐ |
| 🔵 | 238 | [Product of Array Except Self](https://leetcode.com/problems/product-of-array-except-self/) | M | Meta, Amazon, Apple | ⭐ |
| 🔵 | 128 | [Longest Consecutive Sequence](https://leetcode.com/problems/longest-consecutive-sequence/) | M | Google, Amazon | ⭐ |
| 🔵 | 36 | [Valid Sudoku](https://leetcode.com/problems/valid-sudoku/) | M | Uber, Apple | |
| 🔴 | 41 | [First Missing Positive](https://leetcode.com/problems/first-missing-positive/) | H | Amazon, Google | ⭐ |

## §2 Two Pointers

**What it is:** Two fingers on the array — usually one at each end walking toward each other, or one slow and one fast. Turns many O(n²) "check every pair" ideas into a single O(n) sweep.
**Trigger:** sorted input + pair/triplet target; palindromes; in-place removal; "container/area between ends".
**Learn it:** `DSA/05_two_pointers.py` · sorted-array problems almost always hint this.

| Tier | # | Problem | Diff | Companies | ⭐ |
|---|---|---|---|---|---|
| 🟢 | 125 | [Valid Palindrome](https://leetcode.com/problems/valid-palindrome/) | E | Meta | |
| 🟢 | 283 | [Move Zeroes](https://leetcode.com/problems/move-zeroes/) | E | Meta, Apple | |
| 🟢 | 167 | [Two Sum II — Input Array Is Sorted](https://leetcode.com/problems/two-sum-ii-input-array-is-sorted/) | E | Amazon | |
| 🔵 | 15 | [3Sum](https://leetcode.com/problems/3sum/) | M | Meta, Amazon, Google | ⭐ |
| 🔵 | 11 | [Container With Most Water](https://leetcode.com/problems/container-with-most-water/) | M | Amazon, Google | ⭐ |
| 🔴 | 42 | [Trapping Rain Water](https://leetcode.com/problems/trapping-rain-water/) | H | Every FAANG loop | ⭐ |

## §3 Sliding Window

**What it is:** A stretchy frame over a **contiguous** chunk of the array/string. Grow the right edge; when the rule breaks, shrink the left edge. You never restart from scratch — that's the whole trick.
**Trigger:** "longest/shortest/count substring or subarray such that…", fixed size k, "at most k distinct".
**Learn it:** `DSA/07_sliding_window_fixed.py`, `DSA/08_sliding_window_dynamic.py`, `DSA/17_monotonic_queue.py`

| Tier | # | Problem | Diff | Companies | ⭐ |
|---|---|---|---|---|---|
| 🟢 | 643 | [Maximum Average Subarray I](https://leetcode.com/problems/maximum-average-subarray-i/) | E | Google | |
| 🟢 | 121 | [Best Time to Buy and Sell Stock](https://leetcode.com/problems/best-time-to-buy-and-sell-stock/) | E | Amazon, Meta | ⭐ |
| 🔵 | 3 | [Longest Substring Without Repeating Characters](https://leetcode.com/problems/longest-substring-without-repeating-characters/) | M | Amazon, Bloomberg | ⭐ |
| 🔵 | 424 | [Longest Repeating Character Replacement](https://leetcode.com/problems/longest-repeating-character-replacement/) | M | Google | |
| 🔵 | 567 | [Permutation in String](https://leetcode.com/problems/permutation-in-string/) | M | Microsoft | |
| 🔴 | 76 | [Minimum Window Substring](https://leetcode.com/problems/minimum-window-substring/) | H | Meta, Airbnb | ⭐ |
| 🔴 | 239 | [Sliding Window Maximum](https://leetcode.com/problems/sliding-window-maximum/) | H | Amazon, Google | ⭐ |

## §4 Prefix Sum + HashMap

**What it is:** Precompute running totals so "sum of any range" becomes one subtraction. Pair it with a hash map of "prefix sums seen so far" and "count subarrays summing to k" becomes one pass.
**Trigger:** range-sum queries; "subarray sum equals / divisible by k"; balance of 0s and 1s.
**Learn it:** `DSA/06_prefix_sum.py`

| Tier | # | Problem | Diff | Companies | ⭐ |
|---|---|---|---|---|---|
| 🟢 | 303 | [Range Sum Query — Immutable](https://leetcode.com/problems/range-sum-query-immutable/) | E | Bloomberg | |
| 🟢 | 724 | [Find Pivot Index](https://leetcode.com/problems/find-pivot-index/) | E | Meta | |
| 🔵 | 560 | [Subarray Sum Equals K](https://leetcode.com/problems/subarray-sum-equals-k/) | M | Meta, Google | ⭐ |
| 🔵 | 525 | [Contiguous Array](https://leetcode.com/problems/contiguous-array/) | M | Meta | |
| 🔵 | 974 | [Subarray Sums Divisible by K](https://leetcode.com/problems/subarray-sums-divisible-by-k/) | M | Amazon | |

## §5 Stack & Monotonic Stack

**What it is:** A stack is a pile of plates — last in, first out. Perfect for anything *nested* or *undoable*. A **monotonic** stack keeps the pile sorted, which magically answers "next greater/smaller element" for every position in one pass.
**Trigger:** brackets, nesting, undo; "next greater/warmer/cheaper"; histogram areas.
**Learn it:** `DSA/14_stacks.py`, `DSA/15_monotonic_stack.py`

| Tier | # | Problem | Diff | Companies | ⭐ |
|---|---|---|---|---|---|
| 🟢 | 20 | [Valid Parentheses](https://leetcode.com/problems/valid-parentheses/) | E | Everyone | ⭐ |
| 🟢 | 496 | [Next Greater Element I](https://leetcode.com/problems/next-greater-element-i/) | E | Amazon | |
| 🔵 | 155 | [Min Stack](https://leetcode.com/problems/min-stack/) | M | Amazon, Bloomberg | ⭐ |
| 🔵 | 150 | [Evaluate Reverse Polish Notation](https://leetcode.com/problems/evaluate-reverse-polish-notation/) | M | LinkedIn | |
| 🔵 | 739 | [Daily Temperatures](https://leetcode.com/problems/daily-temperatures/) | M | Meta, Amazon | ⭐ |
| 🔴 | 84 | [Largest Rectangle in Histogram](https://leetcode.com/problems/largest-rectangle-in-histogram/) | H | Google, Amazon | ⭐ |

## §6 Binary Search

**What it is:** Guess the middle, throw away the half that can't contain the answer, repeat. Works on sorted arrays — but the senior-level insight is it also works on **answer spaces**: "minimum speed/capacity/days such that condition holds" is binary search on the answer, not the array.
**Trigger:** sorted/rotated input; "O(log n)" hint; "minimum/maximum x such that…".
**Learn it:** `DSA/23_binary_search.py`

| Tier | # | Problem | Diff | Companies | ⭐ |
|---|---|---|---|---|---|
| 🟢 | 704 | [Binary Search](https://leetcode.com/problems/binary-search/) | E | — | |
| 🟢 | 35 | [Search Insert Position](https://leetcode.com/problems/search-insert-position/) | E | — | |
| 🔵 | 74 | [Search a 2D Matrix](https://leetcode.com/problems/search-a-2d-matrix/) | M | Amazon | |
| 🔵 | 33 | [Search in Rotated Sorted Array](https://leetcode.com/problems/search-in-rotated-sorted-array/) | M | Meta, Amazon | ⭐ |
| 🔵 | 153 | [Find Minimum in Rotated Sorted Array](https://leetcode.com/problems/find-minimum-in-rotated-sorted-array/) | M | Meta | ⭐ |
| 🔵 | 875 | [Koko Eating Bananas](https://leetcode.com/problems/koko-eating-bananas/) | M | Google (answer-space BS) | ⭐ |
| 🔵 | 1011 | [Capacity to Ship Packages Within D Days](https://leetcode.com/problems/capacity-to-ship-packages-within-d-days/) | M | Amazon | |
| 🔴 | 4 | [Median of Two Sorted Arrays](https://leetcode.com/problems/median-of-two-sorted-arrays/) | H | Google, Apple | ⭐ |

## §7 Linked List (incl. Fast & Slow Pointers)

**What it is:** A chain of nodes where each holds a pointer to the next. Two recurring tricks: **reverse in place** (rewire pointers one by one) and **fast & slow pointers** (one hops 2, one hops 1 — they meet if and only if there's a cycle; slow lands on the middle when fast hits the end).
**Trigger:** "linked list" in the title; cycle; middle; k-th from end; reorder.
**Learn it:** `DSA/11_linked_list.py`, `DSA/12_linkedlist_reversal.py`, `DSA/13_fast_slow_pointers.py`

| Tier | # | Problem | Diff | Companies | ⭐ |
|---|---|---|---|---|---|
| 🟢 | 206 | [Reverse Linked List](https://leetcode.com/problems/reverse-linked-list/) | E | Everyone | ⭐ |
| 🟢 | 21 | [Merge Two Sorted Lists](https://leetcode.com/problems/merge-two-sorted-lists/) | E | Amazon, Apple | ⭐ |
| 🟢 | 141 | [Linked List Cycle](https://leetcode.com/problems/linked-list-cycle/) | E | Amazon | ⭐ |
| 🟢 | 876 | [Middle of the Linked List](https://leetcode.com/problems/middle-of-the-linked-list/) | E | — | |
| 🔵 | 19 | [Remove Nth Node From End of List](https://leetcode.com/problems/remove-nth-node-from-end-of-list/) | M | Meta | |
| 🔵 | 143 | [Reorder List](https://leetcode.com/problems/reorder-list/) | M | Meta, Amazon | |
| 🔵 | 287 | [Find the Duplicate Number](https://leetcode.com/problems/find-the-duplicate-number/) | M | Google (cycle trick on array) | ⭐ |
| 🔴 | 25 | [Reverse Nodes in k-Group](https://leetcode.com/problems/reverse-nodes-in-k-group/) | H | Meta, Microsoft | ⭐ |

## §8 Trees — DFS & BFS

**What it is:** A tree is folders inside folders. **DFS** dives all the way down one branch before backing up (recursion mirrors this naturally). **BFS** visits floor by floor using a queue — any "level by level" ask is BFS.
**Trigger:** DFS → depth, path, subtree property, ancestor. BFS → level order, right-side view, zigzag.
**Learn it:** `DSA/25_tree_level_order.py`, `DSA/26_tree_preorder.py`–`28_tree_postorder.py`, `DSA/38_dfs.py`, `DSA/39_bfs.py`

| Tier | # | Problem | Diff | Companies | ⭐ |
|---|---|---|---|---|---|
| 🟢 | 226 | [Invert Binary Tree](https://leetcode.com/problems/invert-binary-tree/) | E | Google (famously) | ⭐ |
| 🟢 | 104 | [Maximum Depth of Binary Tree](https://leetcode.com/problems/maximum-depth-of-binary-tree/) | E | — | |
| 🟢 | 543 | [Diameter of Binary Tree](https://leetcode.com/problems/diameter-of-binary-tree/) | E | Meta | |
| 🔵 | 102 | [Binary Tree Level Order Traversal](https://leetcode.com/problems/binary-tree-level-order-traversal/) | M | Amazon, Microsoft | ⭐ |
| 🔵 | 199 | [Binary Tree Right Side View](https://leetcode.com/problems/binary-tree-right-side-view/) | M | Meta | |
| 🔵 | 236 | [Lowest Common Ancestor of a Binary Tree](https://leetcode.com/problems/lowest-common-ancestor-of-a-binary-tree/) | M | Meta, Amazon | ⭐ |
| 🔵 | 105 | [Construct Binary Tree from Preorder and Inorder Traversal](https://leetcode.com/problems/construct-binary-tree-from-preorder-and-inorder-traversal/) | M | Amazon | ⭐ |
| 🔴 | 124 | [Binary Tree Maximum Path Sum](https://leetcode.com/problems/binary-tree-maximum-path-sum/) | H | Meta, Google | ⭐ |
| 🔴 | 297 | [Serialize and Deserialize Binary Tree](https://leetcode.com/problems/serialize-and-deserialize-binary-tree/) | H | Amazon, Google | ⭐ |

## §9 Binary Search Tree

**What it is:** A tree with a promise: everything left is smaller, everything right is bigger. That promise makes search O(log n) and — the key interview fact — **in-order traversal visits values in sorted order**.
**Trigger:** "BST" in the problem; k-th smallest; validate; sorted ↔ tree conversions.
**Learn it:** `DSA/29_bst_ordered_set.py`

| Tier | # | Problem | Diff | Companies | ⭐ |
|---|---|---|---|---|---|
| 🟢 | 700 | [Search in a Binary Search Tree](https://leetcode.com/problems/search-in-a-binary-search-tree/) | E | — | |
| 🟢 | 108 | [Convert Sorted Array to Binary Search Tree](https://leetcode.com/problems/convert-sorted-array-to-binary-search-tree/) | E | — | |
| 🔵 | 235 | [Lowest Common Ancestor of a BST](https://leetcode.com/problems/lowest-common-ancestor-of-a-binary-search-tree/) | M | Meta, Amazon | |
| 🔵 | 98 | [Validate Binary Search Tree](https://leetcode.com/problems/validate-binary-search-tree/) | M | Amazon, Meta | ⭐ |
| 🔵 | 230 | [Kth Smallest Element in a BST](https://leetcode.com/problems/kth-smallest-element-in-a-bst/) | M | Google | ⭐ |

## §10 Heap / Top-K / Two Heaps

**What it is:** A heap always hands you the smallest (or largest) item instantly — a self-sorting to-do pile. Any "top K / K-th / most frequent" is a heap of size K. **Two heaps** (a max-heap for the lower half, min-heap for the upper) track a running median.
**Trigger:** "top K", "K closest", "K-th largest", "most frequent", "median of stream", "merge k sorted".
**Learn it:** `DSA/31_heaps.py`, `DSA/32_two_heaps.py`, `DSA/33_top_k.py`, `DSA/35_k_way_merge.py`, `DSA/22_quickselect.py`

| Tier | # | Problem | Diff | Companies | ⭐ |
|---|---|---|---|---|---|
| 🟢 | 703 | [Kth Largest Element in a Stream](https://leetcode.com/problems/kth-largest-element-in-a-stream/) | E | Amazon | |
| 🟢 | 1046 | [Last Stone Weight](https://leetcode.com/problems/last-stone-weight/) | E | — | |
| 🔵 | 215 | [Kth Largest Element in an Array](https://leetcode.com/problems/kth-largest-element-in-an-array/) | M | Meta, Amazon (also quickselect) | ⭐ |
| 🔵 | 347 | [Top K Frequent Elements](https://leetcode.com/problems/top-k-frequent-elements/) | M | Amazon, Meta | ⭐ |
| 🔵 | 973 | [K Closest Points to Origin](https://leetcode.com/problems/k-closest-points-to-origin/) | M | Meta, Amazon | |
| 🔵 | 621 | [Task Scheduler](https://leetcode.com/problems/task-scheduler/) | M | Meta | |
| 🔴 | 23 | [Merge k Sorted Lists](https://leetcode.com/problems/merge-k-sorted-lists/) | H | Amazon, Google | ⭐ |
| 🔴 | 295 | [Find Median from Data Stream](https://leetcode.com/problems/find-median-from-data-stream/) | H | Google, Amazon (two heaps) | ⭐ |

## §11 Backtracking

**What it is:** Organized brute force: try a choice, recurse deeper, and if it dead-ends, *undo* it and try the next. Draw it as a decision tree — every backtracking problem is "walk this tree, collect valid leaves".
**Trigger:** "generate ALL…", subsets, permutations, combinations, board puzzles, "count valid arrangements".
**Learn it:** `DSA/24_backtracking.py`, `DSA/19_recursion.py`

| Tier | # | Problem | Diff | Companies | ⭐ |
|---|---|---|---|---|---|
| 🔵 | 78 | [Subsets](https://leetcode.com/problems/subsets/) | M | Meta, Amazon | ⭐ |
| 🔵 | 46 | [Permutations](https://leetcode.com/problems/permutations/) | M | Meta, LinkedIn | ⭐ |
| 🔵 | 39 | [Combination Sum](https://leetcode.com/problems/combination-sum/) | M | Amazon, Airbnb | ⭐ |
| 🔵 | 22 | [Generate Parentheses](https://leetcode.com/problems/generate-parentheses/) | M | Amazon, Meta | |
| 🔵 | 79 | [Word Search](https://leetcode.com/problems/word-search/) | M | Amazon, Microsoft | ⭐ |
| 🔵 | 131 | [Palindrome Partitioning](https://leetcode.com/problems/palindrome-partitioning/) | M | Amazon | |
| 🔴 | 51 | [N-Queens](https://leetcode.com/problems/n-queens/) | H | Amazon, Google | ⭐ |

## §12 Trie (Prefix Tree)

**What it is:** A tree where each path from the root spells a word, letter by letter. Makes "does any word start with…" instant. Rare enough that many candidates skip it — which is exactly why it separates offers.
**Trigger:** prefix matching, autocomplete, "add and search word", word dictionaries on boards.
**Learn it:** `DSA/30_tries.py`

| Tier | # | Problem | Diff | Companies | ⭐ |
|---|---|---|---|---|---|
| 🔵 | 208 | [Implement Trie (Prefix Tree)](https://leetcode.com/problems/implement-trie-prefix-tree/) | M | Google, Amazon | ⭐ |
| 🔵 | 211 | [Design Add and Search Words Data Structure](https://leetcode.com/problems/design-add-and-search-words-data-structure/) | M | Meta | |
| 🔴 | 212 | [Word Search II](https://leetcode.com/problems/word-search-ii/) | H | Amazon, Uber (trie + backtracking) | ⭐ |

## §13 Graphs — BFS / DFS / Flood Fill

**What it is:** Nodes + connections — a map of cities and roads. **DFS** explores one road to its end; **BFS** rings outward and therefore finds **shortest paths in unweighted graphs**. A 2-D grid *is* a graph (each cell connects to 4 neighbors) — "count islands" is just flood fill.
**Trigger:** grids with regions; "shortest path" (unweighted → BFS); things spreading (rotting, fire, water); clone/traverse a network.
**Learn it:** `DSA/38_dfs.py`, `DSA/39_bfs.py`, `DSA/10_matrix.py`

| Tier | # | Problem | Diff | Companies | ⭐ |
|---|---|---|---|---|---|
| 🟢 | 733 | [Flood Fill](https://leetcode.com/problems/flood-fill/) | E | Meta | |
| 🔵 | 200 | [Number of Islands](https://leetcode.com/problems/number-of-islands/) | M | Amazon (top-1 asked), Meta | ⭐ |
| 🔵 | 695 | [Max Area of Island](https://leetcode.com/problems/max-area-of-island/) | M | Google | |
| 🔵 | 994 | [Rotting Oranges](https://leetcode.com/problems/rotting-oranges/) | M | Amazon (multi-source BFS) | ⭐ |
| 🔵 | 133 | [Clone Graph](https://leetcode.com/problems/clone-graph/) | M | Meta, Google | ⭐ |
| 🔵 | 417 | [Pacific Atlantic Water Flow](https://leetcode.com/problems/pacific-atlantic-water-flow/) | M | Google | |
| 🔴 | 127 | [Word Ladder](https://leetcode.com/problems/word-ladder/) | H | Amazon, LinkedIn | ⭐ |

## §14 Topological Sort

**What it is:** Ordering tasks when some must come before others — like getting dressed (socks before shoes). Repeatedly take anything with no remaining prerequisites (Kahn's/BFS). If you can't take everything, there's a cycle → impossible.
**Trigger:** prerequisites, dependencies, "valid order", "can you finish", build systems.
**Learn it:** `DSA/40_topological_sort.py`

| Tier | # | Problem | Diff | Companies | ⭐ |
|---|---|---|---|---|---|
| 🔵 | 207 | [Course Schedule](https://leetcode.com/problems/course-schedule/) | M | Amazon, Meta, Google | ⭐ |
| 🔵 | 210 | [Course Schedule II](https://leetcode.com/problems/course-schedule-ii/) | M | Amazon, Meta | ⭐ |
| 🔴 | 269 | [Alien Dictionary](https://leetcode.com/problems/alien-dictionary/) 🔒 | H | Meta, Airbnb (free alt: solve 210 + build the graph from word pairs yourself) | ⭐ |

## §15 Union-Find (Disjoint Set)

**What it is:** Friend circles. `find(x)` asks "who's the leader of x's group", `union(x, y)` merges two groups. With path compression it's effectively O(1) — the fastest way to answer "are these two connected" under a stream of merges.
**Trigger:** connected components, "merge accounts/groups", redundant edges, dynamic connectivity.
**Learn it:** `DSA/41_union_find.py`

| Tier | # | Problem | Diff | Companies | ⭐ |
|---|---|---|---|---|---|
| 🔵 | 547 | [Number of Provinces](https://leetcode.com/problems/number-of-provinces/) | M | Amazon | |
| 🔵 | 684 | [Redundant Connection](https://leetcode.com/problems/redundant-connection/) | M | Google | |
| 🔵 | 721 | [Accounts Merge](https://leetcode.com/problems/accounts-merge/) | M | Meta (very frequent) | ⭐ |

## §16 Intervals

**What it is:** Events on a timeline. Almost every interval problem starts the same way: **sort by start time**, then sweep left to right deciding merge vs. keep vs. drop. "Overlap" means `start2 <= end1`.
**Trigger:** meetings, calendars, ranges, "merge/insert/remove overlapping".
**Learn it:** `DSA/34_intervals.py`, `DSA/59_line_sweep.py`

| Tier | # | Problem | Diff | Companies | ⭐ |
|---|---|---|---|---|---|
| 🟢 | 252 | [Meeting Rooms](https://leetcode.com/problems/meeting-rooms/) 🔒 | E | Meta (free alt: [435](https://leetcode.com/problems/non-overlapping-intervals/) covers the idea) | |
| 🔵 | 56 | [Merge Intervals](https://leetcode.com/problems/merge-intervals/) | M | Meta, Amazon, Google | ⭐ |
| 🔵 | 57 | [Insert Interval](https://leetcode.com/problems/insert-interval/) | M | Google, LinkedIn | |
| 🔵 | 435 | [Non-overlapping Intervals](https://leetcode.com/problems/non-overlapping-intervals/) | M | Meta | ⭐ |
| 🔴 | 253 | [Meeting Rooms II](https://leetcode.com/problems/meeting-rooms-ii/) 🔒 | M | Meta, Amazon (free alt: [1094 Car Pooling](https://leetcode.com/problems/car-pooling/)) | ⭐ |

## §17 Greedy

**What it is:** Take the locally best choice at every step and never look back. Only valid when you can argue the local choice never hurts the global answer — in an interview, *say that argument out loud*; the proof sketch is what they're grading.
**Trigger:** jumps, fuel/gas, partitioning, scheduling where sorting + one pass "feels" right.
**Learn it:** `DSA/37_greedy.py`, `DSA/09_kadane.py`

| Tier | # | Problem | Diff | Companies | ⭐ |
|---|---|---|---|---|---|
| 🔵 | 53 | [Maximum Subarray](https://leetcode.com/problems/maximum-subarray/) | M | Everyone (Kadane) | ⭐ |
| 🔵 | 55 | [Jump Game](https://leetcode.com/problems/jump-game/) | M | Amazon, Meta | ⭐ |
| 🔵 | 45 | [Jump Game II](https://leetcode.com/problems/jump-game-ii/) | M | Google | |
| 🔵 | 134 | [Gas Station](https://leetcode.com/problems/gas-station/) | M | Amazon | |
| 🔵 | 763 | [Partition Labels](https://leetcode.com/problems/partition-labels/) | M | Amazon | |

## §18 Dynamic Programming — 1-D

**What it is:** Recursion + a notebook. Solve tiny cases first, write answers down, build bigger answers from smaller ones. Every 1-D DP is the same interview script: (1) define what `dp[i]` *means* in words, (2) write the recurrence, (3) state base cases. Say those three things before coding.
**Trigger:** "how many ways", "max/min over a sequence of choices", "can it be done" — where today's choice depends on earlier results.
**Learn it:** `DSA/45_dp_1d.py`, `DSA/48_lis.py`, `DSA/55_dp_state_machine.py`

| Tier | # | Problem | Diff | Companies | ⭐ |
|---|---|---|---|---|---|
| 🟢 | 70 | [Climbing Stairs](https://leetcode.com/problems/climbing-stairs/) | E | Everyone's first DP | ⭐ |
| 🟢 | 746 | [Min Cost Climbing Stairs](https://leetcode.com/problems/min-cost-climbing-stairs/) | E | — | |
| 🔵 | 198 | [House Robber](https://leetcode.com/problems/house-robber/) | M | Amazon, Google | ⭐ |
| 🔵 | 213 | [House Robber II](https://leetcode.com/problems/house-robber-ii/) | M | Google | |
| 🔵 | 322 | [Coin Change](https://leetcode.com/problems/coin-change/) | M | Amazon, Meta | ⭐ |
| 🔵 | 139 | [Word Break](https://leetcode.com/problems/word-break/) | M | Meta, Amazon, Google | ⭐ |
| 🔵 | 300 | [Longest Increasing Subsequence](https://leetcode.com/problems/longest-increasing-subsequence/) | M | Google, Microsoft | ⭐ |
| 🔵 | 152 | [Maximum Product Subarray](https://leetcode.com/problems/maximum-product-subarray/) | M | Amazon | |

## §19 Dynamic Programming — 2-D, Knapsack & Strings

**What it is:** Same notebook idea, two dimensions: `dp[i][j]` = answer for "first i of thing A vs first j of thing B" (two strings) or "cell (i, j)" (grids) or "first i items with capacity j" (knapsack). Comparing two strings? It's almost always the LCS/edit-distance family.
**Trigger:** grid paths; two strings compared; "pick items under a budget/target"; palindromic substrings.
**Learn it:** `DSA/49_dp_2d_grid.py`, `DSA/50_dp_string.py`, `DSA/46_knapsack_01.py`, `DSA/47_knapsack_unbounded.py`

| Tier | # | Problem | Diff | Companies | ⭐ |
|---|---|---|---|---|---|
| 🟢 | 62 | [Unique Paths](https://leetcode.com/problems/unique-paths/) | M | Amazon, Google | |
| 🔵 | 64 | [Minimum Path Sum](https://leetcode.com/problems/minimum-path-sum/) | M | Amazon | |
| 🔵 | 1143 | [Longest Common Subsequence](https://leetcode.com/problems/longest-common-subsequence/) | M | Amazon, Google | ⭐ |
| 🔵 | 5 | [Longest Palindromic Substring](https://leetcode.com/problems/longest-palindromic-substring/) | M | Amazon, Microsoft | ⭐ |
| 🔵 | 416 | [Partition Equal Subset Sum](https://leetcode.com/problems/partition-equal-subset-sum/) | M | Meta (0/1 knapsack) | ⭐ |
| 🔵 | 494 | [Target Sum](https://leetcode.com/problems/target-sum/) | M | Meta | |
| 🔴 | 72 | [Edit Distance](https://leetcode.com/problems/edit-distance/) | M | Google, Meta | ⭐ |
| 🔴 | 10 | [Regular Expression Matching](https://leetcode.com/problems/regular-expression-matching/) | H | Google, Meta | ⭐ |

## §20 Bit Manipulation

**What it is:** Numbers are rows of on/off switches. XOR is the star: `x ^ x = 0`, so pairs vanish — that alone solves "everything appears twice except one". Know `n & (n-1)` (drop lowest set bit) and you know 80% of what's asked.
**Trigger:** "appears once/twice", "without using +", powers of two, counting set bits, O(1) space hints.
**Learn it:** `DSA/03_bit_manipulation.py`, `F:\py-learn\BITWISE_CHEATSHEET.md`

| Tier | # | Problem | Diff | Companies | ⭐ |
|---|---|---|---|---|---|
| 🟢 | 136 | [Single Number](https://leetcode.com/problems/single-number/) | E | Amazon | ⭐ |
| 🟢 | 191 | [Number of 1 Bits](https://leetcode.com/problems/number-of-1-bits/) | E | Apple | |
| 🟢 | 268 | [Missing Number](https://leetcode.com/problems/missing-number/) | E | Amazon | |
| 🟢 | 338 | [Counting Bits](https://leetcode.com/problems/counting-bits/) | E | — | |
| 🔵 | 190 | [Reverse Bits](https://leetcode.com/problems/reverse-bits/) | E | Apple | |
| 🔵 | 371 | [Sum of Two Integers](https://leetcode.com/problems/sum-of-two-integers/) | M | — | |

## §21 Design (bonus)

**What it is:** "Build a data structure with these operations at these speeds." The answer is always *composition*: hash map + doubly linked list (LRU), hash map + array (O(1) random), hash map + treemap-ish sorted structure. State the composition first, then code.
**Trigger:** "Design/Implement a … with O(1) …".
**Learn it:** `DSA/36_data_structure_design.py` · Also part of this family, listed earlier: 155 Min Stack, 208 Trie, 295 Median Stream, 703 Kth Largest.

| Tier | # | Problem | Diff | Companies | ⭐ |
|---|---|---|---|---|---|
| 🔵 | 146 | [LRU Cache](https://leetcode.com/problems/lru-cache/) | M | The single most-asked design problem | ⭐ |
| 🔵 | 380 | [Insert Delete GetRandom O(1)](https://leetcode.com/problems/insert-delete-getrandom-o1/) | M | Meta, Amazon | ⭐ |
| 🔵 | 981 | [Time Based Key-Value Store](https://leetcode.com/problems/time-based-key-value-store/) | M | Google (design + binary search) | |

---

## 🔁 How to actually retain this (the part everyone skips)

1. **25-minute rule.** Stuck 25 min → read any solution → close it → rewrite from a blank editor. Reading solutions isn't cheating; *never re-deriving them* is.
2. **Spaced redo.** Every problem you needed help on: redo blank next day, then again on day 7. Three clean solves = owned.
3. **Say the pattern out loud before coding** — in practice and in the real interview. "This is sliding window because we want the longest contiguous substring under a condition." Interviewers grade the recognition, not just the code.
4. **Track a wrong-list.** A plain text file of problem numbers you failed. Your last week before interviews = only that list plus the ⭐ set.
5. **Mocks beat volume.** After ~60% of this sheet, do timed mocks (Pramp/peers/self-timed 35 min). One mock teaches more than five silent solves.

## 📚 Credits & sources

- [Blind 75 / Tech Interview Handbook](https://www.techinterviewhandbook.org/best-practice-questions/) — Yangshun Tay
- [NeetCode Roadmap & 150](https://neetcode.io/practice)
- [Grind 75](https://www.techinterviewhandbook.org/grind75/)
- [Sean Prashad's LeetCode Patterns](https://seanprashad.com/leetcode-patterns/)
- Company tags: aggregated public frequency data — treat as directional, not gospel.

*Problems only. No solutions. That's the point — the struggle is the training.*

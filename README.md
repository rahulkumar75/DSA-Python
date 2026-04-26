# DSA in Python — Interview Prep

![Python](https://img.shields.io/badge/Python-3.x-blue)
![LeetCode](https://img.shields.io/badge/Practice-LeetCode-orange)
![Status](https://img.shields.io/badge/Status-Active-brightgreen)
# ![Target](https://img.shields.io/badge/Target-NPCI-purple)

Structured DSA practice in Python, targeting software engineering and DevOps interviews at product-based companies like NPCI. Solutions organized by topic with time/space complexity noted for every problem.

---

## About me

MCA graduate from BIT Mesra (2024), currently working as a Jr. DevOps Engineer since June 2025. Previously learned DSA concepts in JavaScript (Jan–Jul 2024). This repo is my structured effort to master DSA in Python while simultaneously building automation skills for real DevOps workflows.

- **Education:** MCA — BIT Mesra (2024)
- **Current role:** Jr. DevOps Engineer (June 2025 – present)
- **DSA background:** JavaScript (Jan–Jul 2024)
- **Goal:** NPCI Software / DevOps Engineer roles by 2027

---

## Progress tracker

| Topic          | Easy | Medium | Hard | Total | Status      |
|----------------|------|--------|------|-------|-------------|
| Arrays         | 0    | 0      | 0    | 0     | Upcoming    |
| Strings        | 0    | 0      | 0    | 0     | Upcoming    |
| Hashing        | 0    | 0      | 0    | 0     | Upcoming    |
| Two pointers   | 0    | 0      | 0    | 0     | Upcoming    |
| Sliding window | 0    | 0      | 0    | 0     | Upcoming    |
| Stack / Queue  | 0    | 0      | 0    | 0     | Upcoming    |
| Binary search  | 0    | 0      | 0    | 0     | Upcoming    |
| Linked list    | 0    | 0      | 0    | 0     | Upcoming    |
| Trees          | 0    | 0      | 0    | 0     | Upcoming    |
| **Total**      | **0**| **0**  | **0**| **0** |             |

> Updated weekly every Sunday.

---

## Repo structure

```
dsa-python/
├── 01_arrays/
│   ├── README.md
│   ├── two_sum.py
│   ├── best_time_to_buy_stock.py
│   └── contains_duplicate.py
├── 02_strings/
│   ├── README.md
│   ├── valid_anagram.py
│   └── group_anagrams.py
├── 03_hashing/
│   ├── README.md
│   └── top_k_frequent.py
├── 04_two_pointers/
│   ├── README.md
│   └── valid_palindrome.py
├── 05_sliding_window/
│   ├── README.md
│   └── longest_substring.py
├── 06_stack_queue/
│   ├── README.md
│   └── valid_parentheses.py
├── 07_binary_search/
│   ├── README.md
│   └── binary_search.py
├── 08_linked_list/
│   ├── README.md
│   └── reverse_linked_list.py
├── 09_trees/
│   ├── README.md
│   └── invert_binary_tree.py
├── 10_devops_scripts/
│   ├── README.md
│   ├── log_parser.py
│   ├── config_validator.py
│   └── disk_usage_monitor.py
├── progress.md
└── README.md
```

---

## Solution format

Every `.py` file in this repo follows this exact structure:

```python
# Problem: Two Sum (LeetCode #1)
# Difficulty: Easy
# Link: https://leetcode.com/problems/two-sum/
# Time Complexity: O(n)
# Space Complexity: O(n)

def two_sum(nums, target):
    seen = {}
    for i, num in enumerate(nums):
        diff = target - num
        if diff in seen:
            return [seen[diff], i]
        seen[num] = i
```

---

## DevOps scripts

The `10_devops_scripts/` folder contains Python automation scripts that apply DSA concepts directly to real DevOps use cases:

| Script | Description | DSA concept used |
|--------|-------------|------------------|
| `log_parser.py` | Parse and filter application logs by level/timestamp | Hashing, string manipulation |
| `config_validator.py` | Validate nested YAML/JSON config files | Stack, recursion |
| `disk_usage_monitor.py` | Monitor disk usage and alert on threshold breach | Sorting, queues |

---

## Resources I am using

- [NeetCode.io](https://neetcode.io) — free DSA roadmap + Python video solutions
- [LeetCode](https://leetcode.com) — problem practice (free tier)
- [Striver A2Z DSA Sheet](https://takeuforward.org/strivers-a2z-dsa-course) — topic-wise problem list
- [CS50P — Harvard](https://cs50.harvard.edu/python) — Python fundamentals (completely free)
- [Abhishek Veeramalla](https://www.youtube.com/@AbhishekVeeramalla) — DevOps + Python on YouTube

---

## Commit habit

```
add: two_sum with O(n) hashmap solution
add: valid_anagram using Counter
fix: sliding window edge case in longest_substring
refactor: min_stack using auxiliary stack approach
```

---

*Target: DevOps role / Software Engineer roles | Last updated: April 2026*

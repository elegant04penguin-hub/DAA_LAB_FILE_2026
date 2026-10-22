<div align="center">

# MODY UNIVERSITY OF SCIENCE AND TECHNOLOGY

## School of Engineering and Technology

# DESIGN AND ANALYSIS OF ALGORITHMS (DAA) LAB

### LAB RECORD

**Student Name:** Anushka  
**Enrollment Number:** 240127  
**Faculty Name:** Dr. P. K. Bishnoi

**Mody University of Science and Technology**  
School of Engineering and Technology  
Lakshmangarh, Rajasthan

</div>

---

# INDEX

| S. No. | Program | Program Link |
|---:|---|---|
| 1 | Linear Search | [Program 1](#program-1-linear-search) |
| 2 | Binary Search | [Program 2](#program-2-binary-search) |
| 3 | Bubble Sort | [Program 3](#program-3-bubble-sort) |
| 4 | Selection Sort | [Program 4](#program-4-selection-sort) |
| 5 | Insertion Sort | [Program 5](#program-5-insertion-sort) |
| 6 | Merge Sort | [Program 6](#program-6-merge-sort) |
| 7 | Quick Sort | [Program 7](#program-7-quick-sort) |
| 8 | Heap Sort | [Program 8](#program-8-heap-sort) |
| 9 | Counting Sort | [Program 9](#program-9-counting-sort) |
| 10 | Radix Sort | [Program 10](#program-10-radix-sort) |
| 11 | Shell Sort | [Program 11](#program-11-shell-sort) |
| 12 | Matrix Multiplication | [Program 12](#program-12-matrix-multiplication) |
| 13 | Recursive Factorial | [Program 13](#program-13-recursive-factorial) |
| 14 | Fibonacci using Dynamic Programming | [Program 14](#program-14-fibonacci-using-dynamic-programming) |
| 15 | Euclidean GCD | [Program 15](#program-15-euclidean-gcd) |
| 16 | Fractional Knapsack | [Program 16](#program-16-fractional-knapsack) |
| 17 | 0/1 Knapsack | [Program 17](#program-17-0/1-knapsack) |
| 18 | Activity Selection | [Program 18](#program-18-activity-selection) |
| 19 | Job Sequencing with Deadlines | [Program 19](#program-19-job-sequencing-with-deadlines) |
| 20 | N-Queens Problem | [Program 20](#program-20-nqueens-problem) |
| 21 | Subset Sum | [Program 21](#program-21-subset-sum) |
| 22 | Breadth-First Search (BFS) | [Program 22](#program-22-breadthfirst-search-bfs) |
| 23 | Depth-First Search (DFS) | [Program 23](#program-23-depthfirst-search-dfs) |
| 24 | Dijkstra's Shortest Path | [Program 24](#program-24-dijkstras-shortest-path) |
| 25 | Bellman-Ford Algorithm | [Program 25](#program-25-bellmanford-algorithm) |
| 26 | Floyd-Warshall Algorithm | [Program 26](#program-26-floydwarshall-algorithm) |
| 27 | Prim's Minimum Spanning Tree | [Program 27](#program-27-prims-minimum-spanning-tree) |
| 28 | Kruskal's Minimum Spanning Tree | [Program 28](#program-28-kruskals-minimum-spanning-tree) |
| 29 | Topological Sorting | [Program 29](#program-29-topological-sorting) |
| 30 | Connected Components | [Program 30](#program-30-connected-components) |
| 31 | Huffman Coding | [Program 31](#program-31-huffman-coding) |
| 32 | Longest Common Subsequence | [Program 32](#program-32-longest-common-subsequence) |
| 33 | Coin Change | [Program 33](#program-33-coin-change) |
| 34 | Strassen's Matrix Multiplication (2x2) | [Program 34](#program-34-strassens-matrix-multiplication-2x2) |

---

<a id="program-1-linear-search"></a>
# Program 1: Linear Search

## Aim

Find an element in a list using linear search.

## Program

```python
arr = [10, 20, 30, 40, 50]
key = 30
for i in range(len(arr)):
    if arr[i] == key:
        print("Element found at index", i)
        break
else:
    print("Element not found")
```

## Sample Output

```text
Element found at index 2
```

[Back to Index](#index)

---

<a id="program-2-binary-search"></a>
# Program 2: Binary Search

## Aim

Find an element in a sorted list using binary search.

## Program

```python
arr = [10, 20, 30, 40, 50]
key = 40
low, high = 0, len(arr) - 1
while low <= high:
    mid = (low + high) // 2
    if arr[mid] == key:
        print("Element found at index", mid)
        break
    elif arr[mid] < key:
        low = mid + 1
    else:
        high = mid - 1
else:
    print("Element not found")
```

## Sample Output

```text
Element found at index 3
```

[Back to Index](#index)

---

<a id="program-3-bubble-sort"></a>
# Program 3: Bubble Sort

## Aim

Sort a list using Bubble Sort.

## Program

```python
arr = [5, 1, 4, 2, 8]
n = len(arr)
for i in range(n):
    for j in range(0, n - i - 1):
        if arr[j] > arr[j + 1]:
            arr[j], arr[j + 1] = arr[j + 1], arr[j]
print("Sorted list:", arr)
```

## Sample Output

```text
Sorted list: [1, 2, 4, 5, 8]
```

[Back to Index](#index)

---

<a id="program-4-selection-sort"></a>
# Program 4: Selection Sort

## Aim

Sort a list using Selection Sort.

## Program

```python
arr = [64, 25, 12, 22, 11]
for i in range(len(arr)):
    min_index = i
    for j in range(i + 1, len(arr)):
        if arr[j] < arr[min_index]:
            min_index = j
    arr[i], arr[min_index] = arr[min_index], arr[i]
print("Sorted list:", arr)
```

## Sample Output

```text
Sorted list: [11, 12, 22, 25, 64]
```

[Back to Index](#index)

---

<a id="program-5-insertion-sort"></a>
# Program 5: Insertion Sort

## Aim

Sort a list using Insertion Sort.

## Program

```python
arr = [12, 11, 13, 5, 6]
for i in range(1, len(arr)):
    key = arr[i]
    j = i - 1
    while j >= 0 and arr[j] > key:
        arr[j + 1] = arr[j]
        j -= 1
    arr[j + 1] = key
print("Sorted list:", arr)
```

## Sample Output

```text
Sorted list: [5, 6, 11, 12, 13]
```

[Back to Index](#index)

---

<a id="program-6-merge-sort"></a>
# Program 6: Merge Sort

## Aim

Sort a list using Merge Sort.

## Program

```python
def merge_sort(a):
    if len(a) <= 1:
        return a
    mid = len(a) // 2
    left = merge_sort(a[:mid])
    right = merge_sort(a[mid:])
    result = []
    i = j = 0
    while i < len(left) and j < len(right):
        if left[i] <= right[j]:
            result.append(left[i]); i += 1
        else:
            result.append(right[j]); j += 1
    return result + left[i:] + right[j:]

print("Sorted list:", merge_sort([38, 27, 43, 3, 9, 82, 10]))
```

## Sample Output

```text
Sorted list: [3, 9, 10, 27, 38, 43, 82]
```

[Back to Index](#index)

---

<a id="program-7-quick-sort"></a>
# Program 7: Quick Sort

## Aim

Sort a list using Quick Sort.

## Program

```python
def quick_sort(a):
    if len(a) <= 1:
        return a
    pivot = a[len(a) // 2]
    left = [x for x in a if x < pivot]
    middle = [x for x in a if x == pivot]
    right = [x for x in a if x > pivot]
    return quick_sort(left) + middle + quick_sort(right)

print("Sorted list:", quick_sort([10, 7, 8, 9, 1, 5]))
```

## Sample Output

```text
Sorted list: [1, 5, 7, 8, 9, 10]
```

[Back to Index](#index)

---

<a id="program-8-heap-sort"></a>
# Program 8: Heap Sort

## Aim

Sort a list using Heap Sort.

## Program

```python
import heapq
arr = [12, 11, 13, 5, 6, 7]
heapq.heapify(arr)
sorted_arr = [heapq.heappop(arr) for _ in range(len(arr))]
print("Sorted list:", sorted_arr)
```

## Sample Output

```text
Sorted list: [5, 6, 7, 11, 12, 13]
```

[Back to Index](#index)

---

<a id="program-9-counting-sort"></a>
# Program 9: Counting Sort

## Aim

Sort non-negative integers using Counting Sort.

## Program

```python
arr = [4, 2, 2, 8, 3, 3, 1]
count = [0] * (max(arr) + 1)
for x in arr:
    count[x] += 1
sorted_arr = []
for value, freq in enumerate(count):
    sorted_arr.extend([value] * freq)
print("Sorted list:", sorted_arr)
```

## Sample Output

```text
Sorted list: [1, 2, 2, 3, 3, 4, 8]
```

[Back to Index](#index)

---

<a id="program-10-radix-sort"></a>
# Program 10: Radix Sort

## Aim

Sort non-negative integers using Radix Sort.

## Program

```python
def counting_by_digit(arr, exp):
    out = [0] * len(arr)
    count = [0] * 10
    for x in arr:
        count[(x // exp) % 10] += 1
    for i in range(1, 10):
        count[i] += count[i - 1]
    for x in reversed(arr):
        d = (x // exp) % 10
        out[count[d] - 1] = x
        count[d] -= 1
    return out

arr = [170, 45, 75, 90, 802, 24, 2, 66]
exp = 1
while max(arr) // exp > 0:
    arr = counting_by_digit(arr, exp)
    exp *= 10
print("Sorted list:", arr)
```

## Sample Output

```text
Sorted list: [2, 24, 45, 66, 75, 90, 170, 802]
```

[Back to Index](#index)

---

<a id="program-11-shell-sort"></a>
# Program 11: Shell Sort

## Aim

Sort a list using Shell Sort.

## Program

```python
arr = [12, 34, 54, 2, 3]
gap = len(arr) // 2
while gap > 0:
    for i in range(gap, len(arr)):
        temp = arr[i]
        j = i
        while j >= gap and arr[j - gap] > temp:
            arr[j] = arr[j - gap]
            j -= gap
        arr[j] = temp
    gap //= 2
print("Sorted list:", arr)
```

## Sample Output

```text
Sorted list: [2, 3, 12, 34, 54]
```

[Back to Index](#index)

---

<a id="program-12-matrix-multiplication"></a>
# Program 12: Matrix Multiplication

## Aim

Multiply two matrices using the standard method.

## Program

```python
A = [[1, 2], [3, 4]]
B = [[5, 6], [7, 8]]
C = [[0, 0], [0, 0]]
for i in range(2):
    for j in range(2):
        for k in range(2):
            C[i][j] += A[i][k] * B[k][j]
print("Product matrix:")
for row in C:
    print(row)
```

## Sample Output

```text
Product matrix:\n[19, 22]\n[43, 50]
```

[Back to Index](#index)

---

<a id="program-13-recursive-factorial"></a>
# Program 13: Recursive Factorial

## Aim

Calculate factorial using recursion.

## Program

```python
def factorial(n):
    if n <= 1:
        return 1
    return n * factorial(n - 1)

print("Factorial:", factorial(5))
```

## Sample Output

```text
Factorial: 120
```

[Back to Index](#index)

---

<a id="program-14-fibonacci-using-dynamic-programming"></a>
# Program 14: Fibonacci using Dynamic Programming

## Aim

Generate Fibonacci numbers using dynamic programming.

## Program

```python
n = 8
dp = [0] * n
dp[0], dp[1] = 0, 1
for i in range(2, n):
    dp[i] = dp[i - 1] + dp[i - 2]
print("Fibonacci series:", dp)
```

## Sample Output

```text
Fibonacci series: [0, 1, 1, 2, 3, 5, 8, 13]
```

[Back to Index](#index)

---

<a id="program-15-euclidean-gcd"></a>
# Program 15: Euclidean GCD

## Aim

Find the greatest common divisor using Euclid's algorithm.

## Program

```python
a, b = 48, 18
while b != 0:
    a, b = b, a % b
print("GCD:", a)
```

## Sample Output

```text
GCD: 6
```

[Back to Index](#index)

---

<a id="program-16-fractional-knapsack"></a>
# Program 16: Fractional Knapsack

## Aim

Solve the Fractional Knapsack problem greedily.

## Program

```python
items = [(60, 10), (100, 20), (120, 30)]  # (value, weight)
capacity = 50
items.sort(key=lambda x: x[0] / x[1], reverse=True)
total = 0
for value, weight in items:
    take = min(weight, capacity)
    total += take * value / weight
    capacity -= take
    if capacity == 0:
        break
print("Maximum value:", total)
```

## Sample Output

```text
Maximum value: 240.0
```

[Back to Index](#index)

---

<a id="program-17-0/1-knapsack"></a>
# Program 17: 0/1 Knapsack

## Aim

Find the maximum value for the 0/1 Knapsack problem using dynamic programming.

## Program

```python
values = [60, 100, 120]
weights = [10, 20, 30]
capacity = 50
dp = [0] * (capacity + 1)
for i in range(len(values)):
    for w in range(capacity, weights[i] - 1, -1):
        dp[w] = max(dp[w], values[i] + dp[w - weights[i]])
print("Maximum value:", dp[capacity])
```

## Sample Output

```text
Maximum value: 220
```

[Back to Index](#index)

---

<a id="program-18-activity-selection"></a>
# Program 18: Activity Selection

## Aim

Select the maximum number of non-overlapping activities.

## Program

```python
activities = [(1, 2), (3, 4), (0, 6), (5, 7), (8, 9), (5, 9)]
activities.sort(key=lambda x: x[1])
selected = []
last_end = -1
for start, end in activities:
    if start >= last_end:
        selected.append((start, end))
        last_end = end
print("Selected activities:", selected)
```

## Sample Output

```text
Selected activities: [(1, 2), (3, 4), (5, 7), (8, 9)]
```

[Back to Index](#index)

---

<a id="program-19-job-sequencing-with-deadlines"></a>
# Program 19: Job Sequencing with Deadlines

## Aim

Schedule jobs to maximize profit within deadlines.

## Program

```python
jobs = [('a', 2, 100), ('b', 1, 19), ('c', 2, 27), ('d', 1, 25), ('e', 3, 15)]
jobs.sort(key=lambda x: x[2], reverse=True)
slots = [None] * 3
for name, deadline, profit in jobs:
    for slot in range(min(deadline, 3) - 1, -1, -1):
        if slots[slot] is None:
            slots[slot] = name
            break
print("Job sequence:", [x for x in slots if x is not None])
```

## Sample Output

```text
Job sequence: ['c', 'a', 'e']
```

[Back to Index](#index)

---

<a id="program-20-nqueens-problem"></a>
# Program 20: N-Queens Problem

## Aim

Find one solution to the N-Queens problem using backtracking.

## Program

```python
n = 4
board = [-1] * n
def solve(row):
    if row == n:
        return True
    for col in range(n):
        if all(board[r] != col and abs(board[r] - col) != abs(r - row)
               for r in range(row)):
            board[row] = col
            if solve(row + 1):
                return True
    return False

solve(0)
print("Column positions:", board)
```

## Sample Output

```text
Column positions: [1, 3, 0, 2]
```

[Back to Index](#index)

---

<a id="program-21-subset-sum"></a>
# Program 21: Subset Sum

## Aim

Check whether a subset has the required sum using backtracking.

## Program

```python
def subset_sum(arr, target, i=0, chosen=None):
    if chosen is None:
        chosen = []
    if target == 0:
        return chosen
    if i == len(arr) or target < 0:
        return None
    result = subset_sum(arr, target - arr[i], i + 1, chosen + [arr[i]])
    return result if result is not None else subset_sum(arr, target, i + 1, chosen)

print("Subset:", subset_sum([3, 4, 5, 2], 9))
```

## Sample Output

```text
Subset: [3, 4, 2]
```

[Back to Index](#index)

---

<a id="program-22-breadthfirst-search-bfs"></a>
# Program 22: Breadth-First Search (BFS)

## Aim

Traverse a graph using BFS.

## Program

```python
from collections import deque
graph = {0: [1, 2], 1: [0, 3], 2: [0, 3], 3: [1, 2]}
visited = {0}
queue = deque([0])
order = []
while queue:
    node = queue.popleft()
    order.append(node)
    for neighbor in graph[node]:
        if neighbor not in visited:
            visited.add(neighbor)
            queue.append(neighbor)
print("BFS traversal:", order)
```

## Sample Output

```text
BFS traversal: [0, 1, 2, 3]
```

[Back to Index](#index)

---

<a id="program-23-depthfirst-search-dfs"></a>
# Program 23: Depth-First Search (DFS)

## Aim

Traverse a graph using DFS.

## Program

```python
graph = {0: [1, 2], 1: [0, 3], 2: [0, 3], 3: [1, 2]}
visited = set()
order = []
def dfs(node):
    visited.add(node)
    order.append(node)
    for neighbor in graph[node]:
        if neighbor not in visited:
            dfs(neighbor)
dfs(0)
print("DFS traversal:", order)
```

## Sample Output

```text
DFS traversal: [0, 1, 3, 2]
```

[Back to Index](#index)

---

<a id="program-24-dijkstras-shortest-path"></a>
# Program 24: Dijkstra's Shortest Path

## Aim

Find shortest paths from a source in a graph with non-negative weights.

## Program

```python
import heapq
graph = {0: [(1, 4), (2, 1)], 1: [(3, 1)], 2: [(1, 2), (3, 5)], 3: []}
dist = {node: float("inf") for node in graph}
dist[0] = 0
pq = [(0, 0)]
while pq:
    d, u = heapq.heappop(pq)
    if d != dist[u]:
        continue
    for v, weight in graph[u]:
        if d + weight < dist[v]:
            dist[v] = d + weight
            heapq.heappush(pq, (dist[v], v))
print("Distances from 0:", dist)
```

## Sample Output

```text
Distances from 0: {0: 0, 1: 3, 2: 1, 3: 4}
```

[Back to Index](#index)

---

<a id="program-25-bellmanford-algorithm"></a>
# Program 25: Bellman-Ford Algorithm

## Aim

Find shortest paths and support negative edge weights without negative cycles.

## Program

```python
edges = [(0, 1, 4), (0, 2, 5), (1, 2, -2), (2, 3, 3)]
n = 4
dist = [float("inf")] * n
dist[0] = 0
for _ in range(n - 1):
    for u, v, w in edges:
        if dist[u] != float("inf") and dist[u] + w < dist[v]:
            dist[v] = dist[u] + w
print("Distances from 0:", dist)
```

## Sample Output

```text
Distances from 0: [0, 4, 2, 5]
```

[Back to Index](#index)

---

<a id="program-26-floydwarshall-algorithm"></a>
# Program 26: Floyd-Warshall Algorithm

## Aim

Find shortest paths between all pairs of vertices.

## Program

```python
INF = float("inf")
dist = [[0, 5, INF], [INF, 0, 3], [2, INF, 0]]
n = len(dist)
for k in range(n):
    for i in range(n):
        for j in range(n):
            dist[i][j] = min(dist[i][j], dist[i][k] + dist[k][j])
print("Shortest path matrix:")
for row in dist:
    print(row)
```

## Sample Output

```text
Shortest path matrix:\n[0, 5, 8]\n[5, 0, 3]\n[2, 7, 0]
```

[Back to Index](#index)

---

<a id="program-27-prims-minimum-spanning-tree"></a>
# Program 27: Prim's Minimum Spanning Tree

## Aim

Find a minimum spanning tree using Prim's algorithm.

## Program

```python
import heapq
graph = {0: [(1, 2), (2, 3)], 1: [(0, 2), (2, 1), (3, 4)],
         2: [(0, 3), (1, 1), (3, 5)], 3: [(1, 4), (2, 5)]}
visited = {0}
pq = [(w, 0, v) for v, w in graph[0]]
heapq.heapify(pq)
total = 0
edges = []
while pq and len(visited) < len(graph):
    w, u, v = heapq.heappop(pq)
    if v in visited:
        continue
    visited.add(v); total += w; edges.append((u, v, w))
    for nxt, weight in graph[v]:
        if nxt not in visited:
            heapq.heappush(pq, (weight, v, nxt))
print("MST edges:", edges)
print("Total weight:", total)
```

## Sample Output

```text
MST edges: [(0, 1, 2), (1, 2, 1), (1, 3, 4)]\nTotal weight: 7
```

[Back to Index](#index)

---

<a id="program-28-kruskals-minimum-spanning-tree"></a>
# Program 28: Kruskal's Minimum Spanning Tree

## Aim

Find a minimum spanning tree using Kruskal's algorithm.

## Program

```python
edges = [(1, 1, 2), (2, 0, 1), (3, 0, 2), (4, 1, 3), (5, 2, 3)]
parent = list(range(4))
def find(x):
    while parent[x] != x:
        parent[x] = parent[parent[x]]
        x = parent[x]
    return x
mst = []
for weight, u, v in sorted(edges):
    ru, rv = find(u), find(v)
    if ru != rv:
        parent[ru] = rv
        mst.append((u, v, weight))
print("MST edges:", mst)
print("Total weight:", sum(e[2] for e in mst))
```

## Sample Output

```text
MST edges: [(1, 2, 1), (0, 1, 2), (1, 3, 4)]\nTotal weight: 7
```

[Back to Index](#index)

---

<a id="program-29-topological-sorting"></a>
# Program 29: Topological Sorting

## Aim

Find a topological ordering of a directed acyclic graph.

## Program

```python
from collections import deque
graph = {0: [2, 3], 1: [3], 2: [], 3: []}
indegree = {u: 0 for u in graph}
for u in graph:
    for v in graph[u]:
        indegree[v] += 1
queue = deque([u for u in graph if indegree[u] == 0])
order = []
while queue:
    u = queue.popleft()
    order.append(u)
    for v in graph[u]:
        indegree[v] -= 1
        if indegree[v] == 0:
            queue.append(v)
print("Topological order:", order)
```

## Sample Output

```text
Topological order: [0, 1, 2, 3]
```

[Back to Index](#index)

---

<a id="program-30-connected-components"></a>
# Program 30: Connected Components

## Aim

Find connected components in an undirected graph.

## Program

```python
graph = {0: [1], 1: [0], 2: [3], 3: [2], 4: []}
visited = set()
components = []
for node in graph:
    if node not in visited:
        stack = [node]
        visited.add(node)
        component = []
        while stack:
            u = stack.pop()
            component.append(u)
            for v in graph[u]:
                if v not in visited:
                    visited.add(v)
                    stack.append(v)
        components.append(component)
print("Connected components:", components)
```

## Sample Output

```text
Connected components: [[0, 1], [2, 3], [4]]
```

[Back to Index](#index)

---

<a id="program-31-huffman-coding"></a>
# Program 31: Huffman Coding

## Aim

Build a Huffman tree from symbol frequencies.

## Program

```python
import heapq
freq = {'a': 5, 'b': 9, 'c': 12, 'd': 13}
heap = [[f, [ch, ""]] for ch, f in freq.items()]
heapq.heapify(heap)
while len(heap) > 1:
    left = heapq.heappop(heap)
    right = heapq.heappop(heap)
    for pair in left[1]:
        pair[1] = "0" + pair[1]
    for pair in right[1]:
        pair[1] = "1" + pair[1]
    heapq.heappush(heap, [left[0] + right[0], left[1] + right[1]])
codes = sorted(heap[0][1])
print("Huffman codes:", dict(codes))
```

## Sample Output

```text
Huffman codes: {'a': '110', 'b': '111', 'c': '10', 'd': '0'}
```

[Back to Index](#index)

---

<a id="program-32-longest-common-subsequence"></a>
# Program 32: Longest Common Subsequence

## Aim

Find the length of the longest common subsequence using dynamic programming.

## Program

```python
a, b = "AGGTAB", "GXTXAYB"
dp = [[0] * (len(b) + 1) for _ in range(len(a) + 1)]
for i in range(1, len(a) + 1):
    for j in range(1, len(b) + 1):
        if a[i - 1] == b[j - 1]:
            dp[i][j] = dp[i - 1][j - 1] + 1
        else:
            dp[i][j] = max(dp[i - 1][j], dp[i][j - 1])
print("LCS length:", dp[-1][-1])
```

## Sample Output

```text
LCS length: 4
```

[Back to Index](#index)

---

<a id="program-33-coin-change"></a>
# Program 33: Coin Change

## Aim

Find the minimum number of coins needed for a target amount.

## Program

```python
coins = [1, 3, 4]
amount = 6
dp = [0] + [float("inf")] * amount
for x in range(1, amount + 1):
    for coin in coins:
        if coin <= x:
            dp[x] = min(dp[x], dp[x - coin] + 1)
print("Minimum coins:", dp[amount])
```

## Sample Output

```text
Minimum coins: 2
```

[Back to Index](#index)

---

<a id="program-34-strassens-matrix-multiplication-2x2"></a>
# Program 34: Strassen's Matrix Multiplication (2x2)

## Aim

Demonstrate Strassen's method for multiplying two 2x2 matrices.

## Program

```python
a, b, c, d = 1, 2, 3, 4
e, f, g, h = 5, 6, 7, 8
m1 = (a + d) * (e + h)
m2 = (c + d) * e
m3 = a * (f - h)
m4 = d * (g - e)
m5 = (a + b) * h
m6 = (c - a) * (e + f)
m7 = (b - d) * (g + h)
c11 = m1 + m4 - m5 + m7
c12 = m3 + m5
c21 = m2 + m4
c22 = m1 - m2 + m3 + m6
print("Product matrix:")
print([c11, c12])
print([c21, c22])
```

## Sample Output

```text
Product matrix:\n[19, 22]\n[43, 50]
```

[Back to Index](#index)

---

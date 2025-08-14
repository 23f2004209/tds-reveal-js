---
marp: true
theme: custom
paginate: true
size: 16:9
math: katex
style: |
  .custom-theme {
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    color: white;
  }
  .title-slide {
    text-align: center;
    background: linear-gradient(45deg, #1e3c72, #2a5298);
    color: white;
  }
  .accent {
    color: #ffd700;
    font-weight: bold;
  }
  .code-highlight {
    background: rgba(255, 255, 255, 0.1);
    padding: 20px;
    border-radius: 10px;
    border-left: 4px solid #ffd700;
  }
  .equation-box {
    background: rgba(0, 0, 0, 0.3);
    padding: 20px;
    border-radius: 15px;
    margin: 20px 0;
  }
  h1 {
    font-size: 2.5em;
    margin-bottom: 30px;
  }
  h2 {
    color: #ffd700;
    border-bottom: 2px solid #ffd700;
    padding-bottom: 10px;
  }
---

<!-- _class: title-slide -->
<!-- _paginate: false -->

# Data Structures and Algorithms
## Advanced Analysis and Implementation

**Presented by:** Student  
**Email:** <span class="accent">23f2004209@ds.study.iitm.ac.in</span>  
**Course:** TDS - Term 7  
**Institution:** IIT Madras

---

<!-- _class: custom-theme -->

## Agenda

- **Algorithm Complexity Analysis**
- **Advanced Data Structures**
- **Implementation Strategies**
- **Performance Optimization**
- **Real-world Applications**

---

<!-- _backgroundImage: url('https://images.unsplash.com/photo-1518932945647-7a1c969f8be2?w=1920&h=1080&fit=crop') -->
<!-- _color: white -->

## **Algorithm Complexity**

<div class="equation-box">

### Time Complexity Analysis

$$T(n) = \begin{cases} 
O(1) & \text{if } n \leq 1 \\
T(n-1) + O(n) & \text{if } n > 1
\end{cases}$$

**Solution:** $T(n) = O(n^2)$

</div>

**Key Insights:**
- Recursive algorithms often follow recurrence relations
- Master theorem helps analyze divide-and-conquer algorithms

---

## Advanced Data Structures

### Binary Search Trees

<div class="code-highlight">

**Search Operation Complexity:**
- Best case: $O(\log n)$ - balanced tree
- Worst case: $O(n)$ - skewed tree
- Average case: $O(\log n)$ - random insertions

</div>

### Self-Balancing Trees

$$\text{Height} = \lfloor \log_2(n) \rfloor + 1$$

**Examples:** AVL Trees, Red-Black Trees, B-Trees

---

<!-- _backgroundColor: #2c3e50 -->

## Sorting Algorithms Comparison

| Algorithm | Best Case | Average Case | Worst Case | Space |
|-----------|-----------|--------------|------------|-------|
| Quick Sort | $O(n \log n)$ | $O(n \log n)$ | $O(n^2)$ | $O(\log n)$ |
| Merge Sort | $O(n \log n)$ | $O(n \log n)$ | $O(n \log n)$ | $O(n)$ |
| Heap Sort | $O(n \log n)$ | $O(n \log n)$ | $O(n \log n)$ | $O(1)$ |

<div class="equation-box">

**Comparison-based sorting lower bound:**
$$\Omega(n \log n)$$

</div>

---

<!-- _backgroundImage: url('https://images.unsplash.com/photo-1509048191080-d2ade2d7bb20?w=1920&h=1080&fit=crop') -->
<!-- _color: white -->

## **Graph Algorithms**

### Dijkstra's Algorithm

<div class="equation-box">

**Time Complexity with different data structures:**

- Array: $O(V^2)$
- Binary Heap: $O((V + E) \log V)$
- Fibonacci Heap: $O(E + V \log V)$

Where $V$ = vertices, $E$ = edges

</div>

---

## Dynamic Programming

### Optimal Substructure

<div class="code-highlight">

**Fibonacci Sequence:**
$$F(n) = F(n-1) + F(n-2)$$

**Memoized Solution:** $O(n)$ time, $O(n)$ space

</div>

### Matrix Chain Multiplication

$$M[i,j] = \min_{i \leq k < j}\{M[i,k] + M[k+1,j] + p_{i-1}p_k p_j\}$$

**Time Complexity:** $O(n^3)$

---

<!-- _backgroundColor: #34495e -->

## Hash Tables

### Load Factor and Performance

<div class="equation-box">

**Load Factor:** $\alpha = \frac{n}{m}$

**Expected Operations:**
- Search: $O(1 + \alpha)$
- Insert: $O(1 + \alpha)$
- Delete: $O(1 + \alpha)$

</div>

**Collision Resolution:**
- Chaining: Simple but requires extra memory
- Open Addressing: Better cache performance

---

<!-- _backgroundImage: url('https://images.unsplash.com/photo-1551288049-bebda4e38f71?w=1920&h=1080&fit=crop') -->
<!-- _color: white -->

## **Performance Optimization**

### Cache-Friendly Algorithms

- **Spatial Locality:** Access nearby memory locations
- **Temporal Locality:** Reuse recently accessed data

<div class="equation-box">

**Cache Miss Penalty:**
$$\text{Effective Access Time} = \text{Hit Time} + \text{Miss Rate} \times \text{Miss Penalty}$$

</div>

---

## Real-world Applications

### Search Engines
- **Inverted Index:** $O(1)$ keyword lookup
- **PageRank Algorithm:** $O(n \log n)$ per iteration

### Database Systems
- **B+ Trees:** Optimized for disk access
- **Query Optimization:** Cost-based analysis

### Machine Learning
- **Feature Selection:** $O(2^n)$ brute force vs. heuristics
- **Gradient Descent:** $O(nd)$ per iteration

---

<!-- _class: title-slide -->

## Key Takeaways

1. **Algorithm analysis** is crucial for scalable systems
2. **Data structure choice** significantly impacts performance
3. **Trade-offs** exist between time and space complexity
4. **Real-world constraints** often guide implementation decisions

---

<!-- _class: title-slide -->
<!-- _paginate: false -->

# Thank You

## Questions & Discussion

**Contact:** <span class="accent">23f2004209@ds.study.iitm.ac.in</span>

*"The best algorithm is not always the fastest one, but the one that best fits the problem constraints."*

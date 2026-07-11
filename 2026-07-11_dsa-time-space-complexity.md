# Day Log — DSA: Time Complexity (up to before Big-O Notation)

**Date:** July 11, 2026
**Track:** DSA — Complexity Analysis
**Topic:** Time Complexity — intuition, growth rates, dropping constants/lower-order terms

---

## Key Concepts Learned

### Time Complexity ≠ Time Taken
- Old computer vs M1 MacBook example: same 1,000,000-element array, same linear-search algorithm (target not in array)
- Old machine: 10 sec. M1: 1 sec.
- **Both machines have the same time complexity** — complexity measures how time *grows* with input size, not literal seconds on any one machine

### Growth Rate Comparison
- `O(1)` — flat line (constant, doesn't grow with size)
- `O(log n)` — grows very slowly, flattens out
- `O(n)` — straight diagonal line, grows proportionally

Ordering so far: **O(1) < O(log n) < O(n)**

### Three Rules for Analyzing Complexity
1. Always look for **worst-case** complexity
2. Always look at complexity for **large/infinite data**
3. **Ignore constants** — y=n, y=2n, y=4n all grow linearly regardless of multiplier — we don't care about the actual multiplier, just the growth pattern

### Dropping Constants & Lower-Order Terms
- Example: `O(n³ + log n)` → plug in n = 1 million: `(1 million)³ + log(1 million)` → the log term is tiny compared to n³ → **ignore it** → simplifies to **O(n³)**
- Worked example: `O(7n³ + 4n² + 5n + 6)` = `(n³ + n² + n)` → cross out the less-dominating terms (n² and n) → **O(n³)**
- Rule: **always ignore the less-dominating term**

## Status

✅ Time complexity intuition (hardware-independence) — complete
✅ Growth rate graphs: O(1), O(log n), O(n) — complete
✅ Dropping constants and lower-order terms — complete
⏭️ Next: Formal Big-O notation definition, then Big-Omega, Theta, little-o, little-omega

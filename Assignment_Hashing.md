# Assignment: Hashing

## 1. Properties of an Efficient Hash Function

An efficient hash function should have the following properties:

1. **Deterministic** – The same input must always produce the same hash value.
2. **Fast to compute** – The hash value should be generated quickly.
3. **Uniform distribution** – Keys should be distributed as evenly as possible across the hash table.
4. **Few collisions** – Different keys should rarely produce the same hash value.
5. **Avalanche effect** – A small change in the input should cause a significant change in the hash value.
6. **Consistent with the table size** – The generated hash values should map properly to the available positions in the hash table.

### Example

For a hash table of size `10`, a simple hash function can be:

```text
h(key) = key % 10
```

For example:

```text
h(25) = 25 % 10 = 5
h(37) = 37 % 10 = 7
```

Therefore, 25 is stored at index 5 and 37 is stored at index 7.

---

## 2. Load Factor (α)

The **load factor** of a hash table measures how full the table is.

It is calculated using:

```text
α = n / m
```

Where:

- `α` = load factor
- `n` = number of elements (keys) stored in the hash table
- `m` = total number of slots in the hash table

### Example

If a hash table has **10 slots** and contains **7 elements**:

```text
α = 7 / 10
α = 0.7
```

Therefore, the load factor is **0.7 (70%)**.

### Importance of Load Factor

- A **low load factor** usually means fewer collisions and faster operations.
- A **high load factor** means the table is becoming full, increasing the possibility of collisions.
- When the load factor becomes too high, a hash table may be **resized (rehashing)** to maintain good performance.

## Conclusion

An efficient hash function distributes keys uniformly, is fast to calculate, and minimizes collisions. The load factor indicates how full a hash table is and helps determine when the table should be resized.

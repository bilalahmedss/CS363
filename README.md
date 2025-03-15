# CS363
# Erdős–Rényi \(G(n,p)\) Network Analysis


## 1. Configurations

We examine the following \((n, p)\) pairs:

1. **\(n = 1000\), \(p = 0.01\)**  
2. **\(n = 3000\), \(p = 0.005\)**  
3. **\(n = 5000\), \(p = 0.0025\)**

Each configuration is run 30 times to obtain robust average estimates of:

1. Average Degree  
2. Average Clustering Coefficient  
3. Average Path Length (on the largest connected component)

---

## 2. Theoretical Values
For an Erdős–Rényi \(G(n,p)\) graph, the classic theoretical results are:

- **Average Degree**: $$\langle k\rangle \approx p \times (n - 1)$$

- **Average Clustering**: $$C \approx p$$

- **Approximate Average Path Length**:

  $$
  \ell \approx \frac{\ln(n)}{\ln(\langle k\rangle)}
  \quad (\text{if } \langle k\rangle > 1)
  $$

---

## 3. Empirical Findings

Below are the aggregated results (averaged over 30 runs each) alongside the corresponding theoretical values.

### 3.1. \(n=1000\), \(p=0.01\)

- **Empirical Average Degree**: 10.0244 | **Theoretical**: 9.9900  
- **Empirical Clustering**: 0.0100 | **Theoretical**: 0.01  
- **Empirical Avg Path Length**: 3.2537 | **Theory** ~ 3.0013  

### 3.2. \(n=3000\), \(p=0.005\)

- **Empirical Average Degree**: 14.9552 | **Theoretical**: 14.9950  
- **Empirical Clustering**: 0.0050 | **Theoretical**: 0.005  
- **Empirical Avg Path Length**: 3.2486 | **Theory** ~ 2.9569  

### 3.3. \(n=5000\), \(p=0.0025\)

- **Empirical Average Degree**: 12.5019 | **Theoretical**: 12.4975  
- **Empirical Clustering**: 0.0025 | **Theoretical**: 0.0025  
- **Empirical Avg Path Length**: 3.6516 | **Theory** ~ 3.3724  

---


## 4. Conclusion

1. The **empirical** metrics (average degree, clustering, path length) closely match **theoretical** predictions.  
2. The **degree distributions** center near $$\langle k\rangle \approx p (n-1)$$ and resemble a **Poisson** shape for moderate and larger \(n\).  
3. As \(n\) increases, random‐graph properties (e.g. path lengths, degree fluctuations) converge more tightly to the standard Erdős–Rényi formulas.

---

*For more details and the complete implementation, see the accompanying Jupyter notebook.*
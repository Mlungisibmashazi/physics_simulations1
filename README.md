# Experiment 1: Uniform Random Number Generation

This repository contains my solution for **Experiment 1** of the Physics 344 Computational Physics assignment.

The objective of this experiment is to generate uniformly distributed pseudo-random numbers over the interval **[-1, 1]**, calculate their statistical properties, and analyse their distribution using histograms for different sample sizes.

---

## Objectives

The program performs the following tasks:

- Generates **N** uniformly distributed random numbers using `drand48()`.
- Transforms the generated values to the interval **[-1, 1]**.
- Computes the sample mean.
- Computes the sample variance.
- Divides the interval into **10 equally sized histogram bins**.
- Counts the number of samples in each bin.
- Outputs histogram data for visualization.

---

## Repository Structure

```
.
├── experiment1.c
├── histogram_N10.txt
├── histogram_N20.txt
├── histogram_N50.txt
├── histogram_N100.txt
├── histogram_N1000.txt
├── Figure_1.png
├── Figure_1.pdf
└── README.md
```

### Files

| File | Description |
|------|-------------|
| `experiment1.c` | Source code for Experiment 1 |
| `histogram_N10.txt` | Histogram data for N = 10 |
| `histogram_N20.txt` | Histogram data for N = 20 |
| `histogram_N50.txt` | Histogram data for N = 50 |
| `histogram_N100.txt` | Histogram data for N = 100 |
| `histogram_N1000.txt` | Histogram data for N = 1000 |
| `Figure_1.png` | Histogram subplot for all five sample sizes (PNG) |
| `Figure_1.pdf` | Histogram subplot for all five sample sizes (PDF) |

---

## Compilation

Compile the program using GCC:

```bash
gcc experiment1.c -o experiment1
```

---

## Running the Program

Run the executable by specifying the desired sample size.

Example:

```bash
./experiment1 1000
```

The program calculates:

- Sample mean
- Sample variance
- Histogram frequencies

and writes the histogram data to a text file for plotting.

---

## Results

Histogram data were generated for the following sample sizes:

- N = 10
- N = 20
- N = 50
- N = 100
- N = 1000

The resulting histograms are presented in:

- **Figure_1.png**
- **Figure_1.pdf**

These figures illustrate how the empirical distribution approaches the expected uniform distribution as the sample size increases.

---

## Expected Statistical Behaviour

For a uniform distribution over **[-1,1]**, the theoretical values are

**Expected Mean**

\[
E[X] = 0
\]

**Expected Variance**

\[
\mathrm{Var}(X)=\frac{1}{3}\approx 0.333333
\]

As the sample size increases, the computed mean and variance should converge towards these theoretical values, while the histogram becomes increasingly uniform.

---

## Author

**Mlungisi Blessing Mashazi**

BSc Chemistry (Polymer & Textile Sciences)

Stellenbosch University

---

## License

This repository is provided for educational purposes.

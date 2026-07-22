# Physics 344: Random Number Generation Experiments

This repository contains my solutions for **Experiment 1** and **Experiment 2** of the Physics 344 Computational Physics assignment.

The aim of these experiments is to investigate pseudo-random number generation, compute basic statistical properties, and analyse the resulting distributions using histograms for different sample sizes.

---

# Experiment 1: Uniform Random Number Generation

## Objective

Generate **N** uniformly distributed pseudo-random numbers over the interval **[-1, 1]**.

The program:

- Generates **N** uniformly distributed random numbers using `drand48()`.
- Transforms the generated values to the interval **[-1, 1]**.
- Computes the sample mean.
- Computes the sample variance.
- Divides the interval into **10 equally sized histogram bins**.
- Counts the number of samples in each bin.
- Outputs histogram data for visualization.

### Expected Results

For a uniform distribution on **[-1,1]**,

- **Mean:** 0
- **Variance:** 1/3 ≈ 0.333333

As the sample size increases, the histogram approaches a uniform distribution.

---

# Experiment 2: Discrete Random Number Generation

## Objective

Generate **N** random numbers from the discrete set

\[
Y \in \{0,1,2\}
\]

with probabilities

- P(0) = 1/4
- P(1) = 1/2
- P(2) = 1/4

The program:

- Generates **N** discrete random numbers.
- Computes the sample mean.
- Computes the sample variance.
- Counts the frequency of each outcome.
- Outputs histogram data for visualization.

### Expected Results

The theoretical statistics are

- **Mean:** 1
- **Variance:** 0.5

As the sample size increases, the frequencies approach

| Outcome | Probability |
|---------:|------------:|
| 0 | 25% |
| 1 | 50% |
| 2 | 25% |

---

# Repository Structure

```text
.
├── experiment1.c
├── experiment2.c
│
├── histogram_N10.txt
├── histogram_N20.txt
├── histogram_N50.txt
├── histogram_N100.txt
├── histogram_N1000.txt
│
├── histogram2_N10.txt
├── histogram2_N20.txt
├── histogram2_N50.txt
├── histogram2_N100.txt
├── histogram2_N1000.txt
│
├── plot_experiment1.m
├── plot_experiment2.m
│
├── Figure_1.png
├── Figure_1.pdf
├── Figure_2.png
├── Figure_2.pdf
│
└── README.md
```

---

# Files

| File | Description |
|------|-------------|
| `experiment1.c` | C source code for Experiment 1 |
| `experiment2.c` | C source code for Experiment 2 |
| `plot_experiment1.m` | MATLAB plotting script for Experiment 1 |
| `plot_experiment2.m` | MATLAB plotting script for Experiment 2 |
| `histogram_N*.txt` | Histogram data generated for Experiment 1 |
| `histogram2_N*.txt` | Histogram data generated for Experiment 2 |
| `Figure_1.png` / `Figure_1.pdf` | Histograms for Experiment 1 |
| `Figure_2.png` / `Figure_2.pdf` | Histograms for Experiment 2 |

---

# Compilation

Compile either experiment using GCC.

### Experiment 1

```bash
gcc experiment1.c -o experiment1
```

### Experiment 2

```bash
gcc experiment2.c -o experiment2
```

---

# Running the Programs

### Experiment 1

```bash
./experiment1 1000
```

### Experiment 2

```bash
./experiment2 1000
```

Replace `1000` with any desired sample size, for example:

- 10
- 20
- 50
- 100
- 1000

Each program computes the sample mean and variance and generates the corresponding histogram data file.

---

# Results

Both experiments were performed for the following sample sizes:

- N = 10
- N = 20
- N = 50
- N = 100
- N = 1000

The generated histogram data were plotted in MATLAB.

The figures included in this repository are:

- **Figure_1.png** / **Figure_1.pdf** — Experiment 1
- **Figure_2.png** / **Figure_2.pdf** — Experiment 2

These figures illustrate how the empirical distributions converge towards their respective theoretical distributions as the sample size increases.

---

# Software Used

- C (GCC)
- MATLAB
- Ubuntu Linux

---

# Author

**Mlungisi Blessing Mashazi**

BSc Chemistry (Polymer & Textile Sciences)

Stellenbosch University

---

# License

This repository is provided for educational purposes.

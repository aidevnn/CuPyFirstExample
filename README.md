# CuPy First Example

CuPy SGEMM (Single precision GEneral Matrix Multiplication) test by comparing numpy.dot, cupy.dot and cupy with handwrite cuda kernel

Assuming Python3.7 is already install with package numpy openblas (or numpy with intel mkl) and cupy6.0

### The Output

On my laptop with CPU i7-7500U-2.90GHz (4 threads) and GPU NVIDIA-730MX

```
~/$python sgemm.py --gpu 0 --m 30 --n 40 --k 20
m=30 n=40 k=20
start benchmarking

=============================Result===============================
mklBLAS             time 0.0041728000156581405 ms
hand written kernel time 0.10469760000705719 ms
cuBLAS              time 0.01585279982537031 ms

```

```
~/$python sgemm.py --gpu 0 --m 3840 --n 5120 --k 2560
m=3840 n=5120 k=2560
start benchmarking

=============================Result===============================
mklBLAS             time 677.8629272460937 ms
hand written kernel time 337.38600463867186 ms
cuBLAS              time 150.9483612060547 ms
```

On Google Colab with CPU Intel-Xeon(R)-2.30GHz (2 threads) and GPU NVIDIA-TeslaK80

```
~/$python sgemm.py --gpu 0 --m 30 --n 40 --k 20
m=30 n=40 k=20
start benchmarking

=============================Result===============================
mklBLAS             time 0.00802559992298484 ms
hand written kernel time 0.6085696190595626 ms
cuBLAS              time 0.041068799793720245 ms

```

```
~/$python sgemm.py --gpu 0 --m 3840 --n 5120 --k 2560
m=3840 n=5120 k=2560
start benchmarking

=============================Result===============================
mklBLAS             time 1416.2935302734375 ms
hand written kernel time 54.31614608764649 ms
cuBLAS              time 22.128262329101563 ms
```


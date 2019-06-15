# CuPyFirstExample

CuPy SGEMM (Single precision GEneral Matrix Multiplication) test by comparing numpy.dot, cupy.dot and cupy with handwrite cuda kernel

Assuming Python3.7 is already install with package numpy-mkl and cupy6.0

```
~/$python sgemm.py --gpu 0 --m 3840 --n 5120 --k 2560
```

will produce on my laptop with CPU i7-7500U-2.90GHz (4 threads) and GPU NVIDIA-730MX

```
m=3840 n=5120 k=2560
start benchmarking

=============================Result===============================
mklBLAS             time 677.8629272460937 ms
hand written kernel time 337.38600463867186 ms
cuBLAS              time 150.9483612060547 ms
```

will produce on Google Colab with CPU Intel-Xeon(R)-2.30GHz (2 threads) and GPU NVIDIA-TeslaK80

```
m=3840 n=5120 k=2560
start benchmarking

=============================Result===============================
mklBLAS             time 1416.2935302734375 ms
hand written kernel time 54.31614608764649 ms
cuBLAS              time 22.128262329101563 ms
```


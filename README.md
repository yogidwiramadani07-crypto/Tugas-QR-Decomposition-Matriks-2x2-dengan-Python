# Tugas-QR-Decomposition-Matriks-2x2-dengan-Python

## Deskripsi

Project ini membahas implementasi **QR Decomposition** pada matriks 2x2 menggunakan bahasa pemrograman Python.

QR Decomposition adalah metode dalam aljabar linear untuk memecah suatu matriks menjadi:
```
A=Q⋅R
```
dengan:
```
- Q = matriks ortogonal
- R = matriks segitiga atas
```
---

# Google Colab

Link Google Colab:

```
https://colab.research.google.com/drive/1Vbmj4clRE1zzrZ2_ugG8FVDETWxaNfVC?usp=sharing
```
---

# Matriks Awal

Matriks yang digunakan:

```
A =
[2  1
 1  2]
```
---

# Langkah 1 — Membentuk Vektor

Vektor kolom:
```
a 1 =[2
	  1​]
a 2 =[1
      2]
```
Panjang vektor:

```text
||a1|| = √5
```
Normalisasi vektor:

```text
q1 =
[2/√5
 1/√5]
```


# Langkah 2 — Membentuk Vektor v2

Rumus:

```text
v2 = a2 - (a2 · q1)q1
```
Dot product:

```text
a2 · q1 = 4/√5
```

Hasil:

```text
v2 =
[-3/5
  6/5]
```


# Langkah 3 — Membentuk q2

Panjang vektor:

```text
||v2|| = 3/√5
```

Normalisasi:

```text
q2 =
[-1/√5
  2/√5]
```


# Matriks Q

```text
Q =
[ 2/√5   -1/√5
  1/√5    2/√5]
```

---

# Matriks R

```text
R =
[5/√5   4/√5
 0      3/√5]
```

---

# Implementasi Python

```python
import math
import numpy as np

Q = np.array([
    [2/math.sqrt(5), -1/math.sqrt(5)],
    [1/math.sqrt(5),  2/math.sqrt(5)]
])

R = np.array([
    [5/math.sqrt(5), 4/math.sqrt(5)],
    [0, 3/math.sqrt(5)]
])

hasil = np.dot(Q, R)

print(hasil)
```

---

# Output

```python
[[2. 1.]
 [1. 2.]]
```

Hasil menunjukkan bahwa:
```text
A = Q · R
```
berhasil menghasilkan matriks awal.

---

# Kesimpulan

QR Decomposition dapat digunakan untuk memecah matriks menjadi matriks ortogonal \(Q\) dan matriks segitiga atas \(R\).

Metode ini banyak digunakan dalam:

- Aljabar linear
- Machine Learning
- Penyelesaian sistem persamaan linear
- Komputasi numerik
- Analisis data

# Tugas-QR-Decomposition-Matriks-2x2-dengan-Python
# QR Decomposition Matriks 2x2 dengan Python

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

```txt
[https://colab.research.google.com/](https://colab.research.google.com/drive/1Vbmj4clRE1zzrZ2_ugG8FVDETWxaNfVC?usp=sharing)
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

# Langkah 1 — Membentuk Vektor \(a_1\)

Vektor kolom:

a
1
	​

=[
2
1
	​

]a
2
	​

=[
1
2]

Panjang vektor:

\[
||a_1|| = \sqrt{2^2 + 1^2}
\]

\[
||a_1|| = \sqrt{5}
\]

Normalisasi vektor:

\[
q_1 =
\frac{a_1}{||a_1||}
\]

\[
q_1 =
\begin{bmatrix}
\frac{2}{\sqrt{5}} \\
\frac{1}{\sqrt{5}}
\end{bmatrix}
\]

---

# Langkah 2 — Membentuk Vektor \(v_2\)

\[
a_2 =
\begin{bmatrix}
1 \\
2
\end{bmatrix}
\]

Rumus:

\[
v_2 = a_2 - (a_2 \cdot q_1)q_1
\]

Hasil:

\[
v_2 =
\begin{bmatrix}
-\frac{3}{5} \\
\frac{6}{5}
\end{bmatrix}
\]

---

# Langkah 3 — Membentuk \(q_2\)

Panjang vektor:

\[
||v_2|| =
\sqrt{
\left(-\frac{3}{5}\right)^2 +
\left(\frac{6}{5}\right)^2
}
\]

\[
||v_2|| =
\frac{3}{\sqrt{5}}
\]

Normalisasi:

\[
q_2 =
\frac{v_2}{||v_2||}
\]

\[
q_2 =
\begin{bmatrix}
-\frac{1}{\sqrt{5}} \\
\frac{2}{\sqrt{5}}
\end{bmatrix}
\]

---

# Matriks Q

\[
Q =
\begin{bmatrix}
\frac{2}{\sqrt{5}} & -\frac{1}{\sqrt{5}} \\
\frac{1}{\sqrt{5}} & \frac{2}{\sqrt{5}}
\end{bmatrix}
\]

---

# Matriks R

\[
R =
\begin{bmatrix}
\frac{5}{\sqrt{5}} & \frac{4}{\sqrt{5}} \\
0 & \frac{3}{\sqrt{5}}
\end{bmatrix}
\]

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

\[
A = Q \cdot R
\]

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

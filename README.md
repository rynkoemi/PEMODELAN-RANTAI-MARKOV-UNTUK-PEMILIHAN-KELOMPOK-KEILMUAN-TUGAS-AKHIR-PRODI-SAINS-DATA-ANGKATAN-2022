# PEMODELAN-RANTAI-MARKOV-UNTUK-PEMILIHAN-KELOMPOK-KEILMUAN-TUGAS-AKHIR-PRODI-SAINS-DATA-ANGKATAN-2022
Proyek ini merupakan analisis menggunakan **Rantai Markov (Markov Chain)** untuk memodelkan perpindahan minat mahasiswa Sains Data dari Semester 4 ke Semester 7. Analisis dilakukan pada dua kelompok keilmuan:

* **X₁ — Pemodelan & Simulasi Data**
* **X₂ — Computer Vision**

Model Markov digunakan untuk memahami pola perpindahan minat, stabilitas pilihan keilmuan, dan prediksi kecenderungan jangka panjang mahasiswa berdasarkan data kuesioner.

---

## 📁 Struktur Repository

```
📦 project-root/
├── data/
│   └── form_responses.csv
├── R/
│   └── markov-analysis.R
├── figures/
│   └── transition-diagram.png
└── README.md
```

---

## 🔍 Ringkasan Hasil Utama

| Komponen Analisis    | Hasil                  |
| -------------------- | ---------------------- |
| Jumlah mahasiswa     | 42                     |
| State                | X₁, X₂                 |
| Dominan Semester 4   | X₁ (61.90%)            |
| Dominan Semester 7   | X₁ (64.29%)            |
| Perpindahan terbesar | X₂ → X₁ (18.75%)       |
| Matriks P            | [                      |
| \begin{bmatrix}      |                        |
| 0.9231 & 0.0769 \    |                        |
| 0.1875 & 0.8125      |                        |
| \end{bmatrix}        |                        |
| ]                    |                        |
| P⁵                   | X₁: 0.7717, X₂: 0.2283 |
| Distribusi stasioner | π = (0.7091, 0.2909)   |
| Klasifikasi state    | Semua recurrent        |

---

## 🧮 Metode Analisis

Analisis menggunakan konsep inti rantai Markov dengan elemen-elemen berikut:

### **State Space**

```
S = { X1, X2 }
```

### **Transition Matrix**

[
P=
\begin{bmatrix}
0.9231 & 0.0769 \
0.1875 & 0.8125
\end{bmatrix}
]

### **n-step Transition**

[
P^5=
\begin{bmatrix}
0.7717 & 0.2283 \
0.5564 & 0.4463
\end{bmatrix}
]

### **Steady-State Distribution**

[
\pi = (0.7091, 0.2909)
]

### **State Classification**

Semua state adalah *recurrent* karena dapat saling dicapai dan memiliki nilai stasioner positif.

---

## 🛠 Teknologi & Library

### **R**

* `dplyr`
* `expm`
* `DiagrammeR`
* `matrixcalc` *(opsional)*

---

## 📊 Visualisasi

Diagram transisi menggambarkan arah perpindahan minat mahasiswa:

```
   X1 ↺ 0.9231           0.0769 ➜ X2
   X2 ↺ 0.8125           0.1875 ➜ X1
```

Versi grafik disimpan pada folder `figures/`.

---

## 🚀 Cara Menjalankan Analisis

Clone repository:

```bash
git clone https://github.com/USERNAME/REPO-NAME.git
```

Masuk ke folder project:

```bash
cd REPO-NAME
```

Jalankan script utama di R:

```r
source("R/markov-analysis.R")
```


---

## 👤 Pengembang

**Rayan Koemi Karuby**
Program Studi Sains Data
rayan.122450038@student.itera.ac.id

**Patricia Leondrea Diajeng Putri**
Program Studi Sains Data
patricia.122450050@student.itera.ac.id

Azizah Kusumah Putri
Program Studi Sains Data
azizah.122450068@student.itera.ac.id

**Renta Siahaan**
Program Studi Sains Data
renta.122450070@student.itera.ac.id

**Naufal Fakhri**
Program Studi Sains Data
naufal.122450089@student.itera.ac.id

---



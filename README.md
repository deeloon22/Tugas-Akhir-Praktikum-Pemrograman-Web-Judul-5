# 🌌 Kalkulator Interaktif Modern  
### _Praktikum Pemrograman Web — JavaScript Dasar_

---

## 🎯 Deskripsi Proyek
Proyek ini dibuat sebagai implementasi materi **JavaScript Dasar** pada Praktikum Pemrograman Web.  
Aplikasi ini adalah **Kalkulator Interaktif Modern** dengan tampilan futuristik berbasis HTML, CSS, dan JavaScript.  

Kalkulator ini mendukung:
- Operasi dasar: `+`, `-`, `×`, `÷`
- Operator precedence (prioritas matematika)
- Memory function (MC, MR, M+, M-)
- Riwayat perhitungan (History)
- Keyboard support
- Tampilan modern (glassmorphism + responsive)

---

# 🌐 Tampilan Web
<img width="1366" height="720" alt="image" src="https://github.com/user-attachments/assets/64746799-4b79-494e-a09c-971897a54f3b" />

<img width="1366" height="720" alt="image" src="https://github.com/user-attachments/assets/742eef4b-83ed-4e0f-8339-b09e34ed9765" />


# 🧠 Konsep JavaScript yang Digunakan

### ✔️ Variabel untuk menyimpan state  
```javascript
let displayValue = '0';
let expression = '';
let memory = 0;
let history = [];
```

### ✔️ Manipulasi DOM  
Mengubah isi layar kalkulator secara dinamis:
```javascript
document.getElementById('display').textContent = displayValue;
```

### ✔️ Fungsi Modular  
Program dibagi ke banyak fungsi kecil seperti:
- inputDigit()
- inputDecimal()
- setOperation()
- calculate()
- memoryAdd(), memorySubtract()
- toggleHistory()

### ✔️ Event Listener  
Menangani input keyboard:
```javascript
document.addEventListener('keydown', function(e) { ... });
```

### ✔️ Logika & Operator  
Program menerapkan *operator precedence* (× & ÷ lebih dulu dari + & -).

### ✔️ Array Handling  
Untuk menyimpan history:
```javascript
history.unshift(calculation);
```

---

# 🧩 Step-by-Step Cara Kerja Program

## 🟦 1. Inisialisasi Variabel  
Program mengatur:
- nilai awal layar = 0  
- ekspresi kosong  
- memory = 0  
- history = []  

---

## 🟩 2. Input Angka  
Saat tombol angka ditekan:
```javascript
displayValue = displayValue === '0' ? digit : displayValue + digit;
```

---

## 🟨 3. Input Titik Desimal  
Mencegah lebih dari satu titik:
```javascript
if (!displayValue.includes('.')) displayValue += '.';
```

---

## 🟥 4. Memilih Operator  
Saat menekan `+ - × ÷`:
```javascript
expression += displayValue + nextOperation;
waitingForOperand = true;
```

---

## 🟪 5. Evaluasi Ekspresi  
Program menggunakan algoritma *shunting-yard* untuk memprioritaskan operator:
- Membaca input
- Mengubah menjadi postfix
- Menghitung hasil

Pembagian 0 ditangani khusus:
```
Error: Div by 0
```

---

## 🟫 6. History Perhitungan  
Menampilkan 5 riwayat terbaru:
```javascript
history.unshift(expr + ' = ' + result);
```

---

## 🟧 7. Memory Calculator  
Sudah seperti kalkulator asli:
- **MC** → hapus memory  
- **MR** → tampilkan memory  
- **M+** → tambah memory  
- **M-** → kurangi memory  

---

## 🟦 8. Keyboard Support  
- Enter = sama dengan  
- Escape = clear  
- Backspace = CE  
- 0–9 = angka  
- + - * / = operator  

---

## 🟩 9. Antarmuka Modern  
Menggunakan:
- Gradient background  
- Glassmorphism  
- Shadow soft  
- Responsive CSS  
- Grid layout  

---

# 📁 Struktur Folder  
```
/project-folder
│── TugasAkhir.html
│── README.md
```



# AI Agent Guidelines

Repository ini berisi standar dan aturan penggunaan AI Assistant (seperti CLI agent, IDE assistant, dll) dalam proses development.

Tujuannya adalah agar penggunaan AI:

* Tetap **aman (secure)**
* Konsisten dengan **standar engineering**
* Tidak merusak **arsitektur dan kualitas codebase**

---

# 🎯 Tujuan Utama

Panduan ini dibuat untuk membantu engineer dari level **junior hingga senior** agar:

* Menggunakan AI secara efektif (bukan asal generate code)
* Menghindari kesalahan umum saat pakai AI
* Menjaga keamanan data & credential
* Tetap mengikuti standar project

---


# 🧱 Standar Engineering

AI harus mengikuti:

* arsitektur project
* coding standard
* struktur package

Lihat detail di:

👉 `AGENTS.md`

---

# 📘 Cara Menggunakan AGENTS.md

Bagian ini menjelaskan **cara praktis** memakai `AGENTS.md` saat bekerja dengan AI (CLI maupun IDE).

---

## 📍 1. Dimana Menyimpan File

* Simpan `AGENTS.md` di **root repository** (satu level dengan `.git`, `README.md`, dll)

Contoh:

```
/project-root
  ├── AGENTS.md
  ├── README.md
  ├── src/
  └── pom.xml
```

👉 Tujuannya agar mudah ditemukan dan (jika didukung) otomatis dibaca oleh AI

---

## 🤖 2. Apakah AI Otomatis Membaca AGENTS.md?

Jawabannya: **tergantung tool yang kamu pakai**

### 🔹 CLI (Gemini CLI, dll)

* ❌ Umumnya **TIDAK otomatis** membaca `AGENTS.md`
* ✅ Kamu **HARUS menyebutkan secara eksplisit** di prompt

Contoh:

```
Ikuti aturan di AGENTS.md, bantu saya buat service baru sesuai standar project ini
```

---

### 🔹 IDE (IntelliJ, VSCode, dll)

* Beberapa AI:

  * ✅ bisa membaca file di repo sebagai context
  * ❌ tapi tidak selalu menjadikannya “rule utama”

👉 Jadi tetap disarankan:

```
Follow AGENTS.md in this repository
```

---

## 🧠 3. Kapan Harus Menyebut AGENTS.md?

### WAJIB menyebut jika:

* generate code baru
* refactor
* ubah arsitektur
* buat API / service

### Opsional jika:

* tanya konsep umum
* debugging kecil

👉 Rule praktis:

> Kalau perubahan berdampak ke codebase → sebut AGENTS.md

---

## ✍️ 4. Contoh Prompt (Salah vs Benar)

### ❌ Tanpa AGENTS.md

```
Buatkan controller Spring Boot
```

👉 Risiko:

* tidak pakai MapStruct
* expose entity
* tidak sesuai standar

---

### ✅ Dengan AGENTS.md

```
Ikuti AGENTS.md, buatkan controller Spring Boot lengkap dengan DTO, mapper, dan response standard
```

👉 Hasil:

* lebih konsisten
* sesuai arsitektur

---

## 🔄 5. Jika AGENTS.md Belum Cover Kebutuhan

Kadang kebutuhan belum ada di guideline.

### Cara yang benar:

```
Ikuti AGENTS.md, dan untuk bagian X gunakan pendekatan Y karena belum ada di guideline
```

atau:

```
AGENTS.md belum mengatur ini, tolong sarankan approach terbaik yang tetap konsisten dengan project
```

👉 Jangan langsung override tanpa penjelasan

---

## ⚠️ 6. Jika AI Melanggar AGENTS.md

Langsung koreksi:

```
Kode ini tidak sesuai AGENTS.md (misalnya masih pakai @Autowired), tolong perbaiki
```

👉 Ini penting untuk menjaga konsistensi

---

## 🧩 7. Tips Praktis (Biar Nggak Ribet)

* Simpan snippet prompt:

```
Ikuti AGENTS.md di repo ini
```

* Gunakan sebagai prefix setiap prompt penting

* Biasakan review hasil AI dengan referensi AGENTS.md

---

## 🎯 Tujuan Penggunaan

Dengan menggunakan `AGENTS.md` secara benar:

* AI lebih terarah
* hasil lebih konsisten
* mengurangi bug
* meningkatkan keamanan

---

## 📌 Ringkasan

* Simpan di root project
* CLI: HARUS disebut manual
* IDE: kadang otomatis, tapi tetap lebih aman disebut
* Gunakan untuk semua perubahan penting
* Koreksi jika AI tidak patuh

---

# 🚫 Kesalahan Umum

Beberapa kesalahan yang sering terjadi:

* Langsung percaya AI
* Copy-paste config sensitif
* Jalankan command tanpa review
* Mengubah terlalu banyak file sekaligus

---

# ✅ Best Practice

* Gunakan AI untuk mempercepat, bukan menggantikan
* Selalu review hasil AI
* Gunakan prompt yang jelas
* Jaga keamanan data

---

# 🧠 Mindset

Gunakan AI seperti:

> Junior engineer yang cepat, tapi tetap perlu di-review

---

# 📌 Ringkasan

AI itu powerful, tapi:

* bisa salah
* bisa berbahaya jika tidak dikontrol

Gunakan dengan bijak, dan selalu ikuti aturan di `AGENTS.md`

---

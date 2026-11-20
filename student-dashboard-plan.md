# Plan: Dashboard Pelajar Sijil Teknologi Maklumat
## Kolej Komuniti Pasir Gudang

## Overview

Membina sebuah dashboard HTML statik satu halaman (single-page) yang memaparkan maklumat pelajar program **Sijil Teknologi Maklumat** di **Kolej Komuniti Pasir Gudang**. Dashboard ini menggunakan data pelajar yang ditulis terus dalam JavaScript (hardcoded), dengan paparan yang merangkumi maklumat asas pelajar, prestasi akademik, dan statistik keseluruhan dengan carta interaktif.

**Teknologi:**
- HTML5 + CSS3 (inline dalam satu fail)
- Bootstrap 5 (via CDN) — susun atur dan komponen UI
- Chart.js (via CDN) — carta interaktif
- JavaScript (vanilla) — logik paparan dan penapisan data

**Output:** Satu fail `index.html` yang boleh dibuka terus dalam pelayar web tanpa pelayan.

---

## Data Contoh Pelajar (50 Rekod)

| No. Matrik | Nama | Jantina | Semester | CGPA | Status |
|---|---|---|---|---|---|
| STM2024001 | Ahmad Faris bin Zainal | Lelaki | 3 | 3.45 | Aktif |
| STM2024002 | Nurul Ain binti Hamid | Perempuan | 3 | 3.80 | Aktif |
| STM2024003 | Muhammad Haziq bin Rosli | Lelaki | 2 | 2.95 | Aktif |
| STM2024004 | Siti Noorhafilah binti Aziz | Perempuan | 4 | 3.60 | Aktif |
| STM2024005 | Mohd Azri bin Kamarudin | Lelaki | 1 | 2.50 | Aktif |
| STM2024006 | Farah Nabilah binti Yusof | Perempuan | 2 | 3.20 | Aktif |
| STM2024007 | Syafiq Aiman bin Idris | Lelaki | 4 | 2.10 | Tidak Aktif |
| STM2024008 | Noor Hidayah binti Sulaiman | Perempuan | 1 | 3.90 | Aktif |
| STM2024009 | Hafizuddin bin Othman | Lelaki | 3 | 2.70 | Tangguh |
| STM2024010 | Amirah Sofea binti Ramli | Perempuan | 2 | 3.55 | Aktif |
| STM2024011 | Irfan Izzat bin Zulkifli | Lelaki | 4 | 3.10 | Aktif |
| STM2024012 | Nur Izzati binti Mohd Noor | Perempuan | 1 | 2.85 | Aktif |
| STM2024013 | Khairul Anwar bin Bakar | Lelaki | 3 | 2.30 | Tangguh |
| STM2024014 | Zulaikha binti Abd Rahman | Perempuan | 4 | 3.75 | Aktif |
| STM2024015 | Danish Haikal bin Mazlan | Lelaki | 2 | 3.00 | Aktif |
| STM2024016 | Aisyah Humaira binti Ghazali | Perempuan | 1 | 3.65 | Aktif |
| STM2024017 | Muhamad Aqil bin Sapuan | Lelaki | 2 | 2.40 | Tangguh |
| STM2024018 | Nursyafiqah binti Ismail | Perempuan | 3 | 3.30 | Aktif |
| STM2024019 | Luqmanul Hakim bin Nordin | Lelaki | 4 | 2.80 | Aktif |
| STM2024020 | Sofiah binti Zainudin | Perempuan | 1 | 3.50 | Aktif |
| STM2024021 | Hazwan Fitri bin Hashim | Lelaki | 2 | 3.15 | Aktif |
| STM2024022 | Nabilah Zahirah binti Musa | Perempuan | 3 | 2.60 | Tidak Aktif |
| STM2024023 | Afiq Danial bin Alias | Lelaki | 4 | 3.90 | Aktif |
| STM2024024 | Nuratikah binti Jaafar | Perempuan | 1 | 2.75 | Aktif |
| STM2024025 | Zikri Haikal bin Zainol | Lelaki | 2 | 3.40 | Aktif |
| STM2024026 | Fatin Liyana binti Halim | Perempuan | 3 | 3.70 | Aktif |
| STM2024027 | Ridhwan Azizi bin Rashid | Lelaki | 4 | 2.20 | Tangguh |
| STM2024028 | Khairunnisa binti Omar | Perempuan | 1 | 3.85 | Aktif |
| STM2024029 | Amir Hamzah bin Yusri | Lelaki | 2 | 2.65 | Aktif |
| STM2024030 | Izyan Izzati binti Kamarul | Perempuan | 3 | 3.25 | Aktif |
| STM2024031 | Farhan Hisyam bin Latif | Lelaki | 4 | 3.55 | Aktif |
| STM2024032 | Siti Maisarah binti Daud | Perempuan | 1 | 2.90 | Aktif |
| STM2024033 | Nazri Hakimi bin Ramlan | Lelaki | 2 | 2.15 | Tidak Aktif |
| STM2024034 | Nurul Hidayah binti Fauzi | Perempuan | 3 | 3.45 | Aktif |
| STM2024035 | Fitri Asyraf bin Mansor | Lelaki | 4 | 3.00 | Aktif |
| STM2024036 | Atiqah Nadhirah binti Salleh | Perempuan | 1 | 3.60 | Aktif |
| STM2024037 | Shahril Nizam bin Bahari | Lelaki | 2 | 2.85 | Tangguh |
| STM2024038 | Nurul Fatihah binti Zakaria | Perempuan | 3 | 3.95 | Aktif |
| STM2024039 | Hafiz Amsyar bin Abdul Aziz | Lelaki | 4 | 3.20 | Aktif |
| STM2024040 | Syazwani binti Zulkarnain | Perempuan | 1 | 2.55 | Aktif |
| STM2024041 | Izzuddin Amsyar bin Jamal | Lelaki | 2 | 3.70 | Aktif |
| STM2024042 | Noor Syafiqah binti Hamzah | Perempuan | 3 | 2.40 | Tidak Aktif |
| STM2024043 | Muhaimin Rasyid bin Lokman | Lelaki | 4 | 3.35 | Aktif |
| STM2024044 | Fauziah binti Suhaimi | Perempuan | 1 | 3.80 | Aktif |
| STM2024045 | Ezwan Fitri bin Mohd Zain | Lelaki | 2 | 2.70 | Aktif |
| STM2024046 | Nurnajwa binti Kamarol | Perempuan | 3 | 3.50 | Aktif |
| STM2024047 | Syamil Hafizi bin Ghani | Lelaki | 4 | 2.95 | Tangguh |
| STM2024048 | Hanis Syazwani binti Rashdan | Perempuan | 1 | 3.40 | Aktif |
| STM2024049 | Arif Hakimi bin Zulkefli | Lelaki | 2 | 3.65 | Aktif |
| STM2024050 | Nurliyana binti Abd Ghani | Perempuan | 3 | 2.80 | Aktif |

---

## Struktur Dashboard

### Bahagian 1 — Header & Navbar
- Logo / nama kolej: **Kolej Komuniti Pasir Gudang**
- Nama program: **Sijil Teknologi Maklumat**
- Warna tema: biru gelap (navbar) + putih (kandungan)

### Bahagian 2 — KPI Cards (4 kad)
- Jumlah Pelajar — dikira dari data
- Pelajar Aktif — dikira dari data
- Purata CGPA — purata semua CGPA
- Kadar Kelulusan (%) — peratusan pelajar CGPA ≥ 2.0

### Bahagian 3 — Carta & Statistik
- **Pie Chart:** Agihan Jantina (Lelaki vs Perempuan)
- **Bar Chart:** Agihan Gred CGPA (A / B / C / D)
- **Doughnut Chart:** Status Pelajar (Aktif / Tidak Aktif / Tangguh)

### Bahagian 4 — Jadual Pelajar
- Carian nama (real-time)
- Penapisan semester (dropdown)
- Kolum: No. Matrik, Nama, Jantina, Semester, CGPA, Status
- Status sebagai badge berwarna

### Bahagian 5 — Footer
- Nama kolej dan tahun semasa

---

## Sub-Tasks

### Sub-Task 1: Struktur Asas HTML & Header
- **Status:** `[ ] pending`
- **Intent:** Menyediakan rangka fail HTML dengan header, navbar, dan metadata yang menggambarkan identiti kolej dan program.
- **Expected Outcomes:**
  - Fail `index.html` wujud dengan struktur HTML5 lengkap
  - Header memaparkan nama kolej, nama program
  - Bootstrap 5 dan Chart.js berjaya dimuatkan via CDN
- **Todo List:**
  1. Cipta fail `index.html` di folder playground
  2. Tambah `<head>` dengan meta tag, tajuk, dan CDN links (Bootstrap 5, Chart.js, Bootstrap Icons)
  3. Bina `<header>` navbar dengan nama "Kolej Komuniti Pasir Gudang" dan "Sijil Teknologi Maklumat"
  4. Tambah warna tema biru gelap menggunakan CSS dalam `<style>`
- **Relevant Context:** Projek baru dari awal, tiada fail sedia ada.

---

### Sub-Task 2: Data Pelajar (JavaScript Hardcoded)
- **Status:** `[ ] pending`
- **Intent:** Menyediakan set data 50 pelajar yang tepat seperti dalam jadual Data Contoh di atas dalam format JavaScript array.
- **Expected Outcomes:**
  - `const dataPelajar = [...]` mengandungi tepat 50 rekod seperti dalam seksyen "Data Contoh Pelajar"
  - Setiap rekod mengandungi: `noMatrik`, `nama`, `jantina`, `semester`, `cgpa`, `status`
- **Todo List:**
  1. Tulis `const dataPelajar = [...]` dalam `<script>` tag
  2. Masukkan 15 rekod pelajar mengikut jadual Data Contoh di atas dengan tepat
- **Relevant Context:** Data ini digunakan oleh Sub-Task 3, 4, dan 5.

---

### Sub-Task 3: KPI Cards (Kad Ringkasan)
- **Status:** `[ ] pending`
- **Intent:** Memaparkan 4 angka utama pada bahagian atas dashboard dikira secara dinamik dari data.
- **Expected Outcomes:**
  - 4 kad dipaparkan: Jumlah Pelajar, Pelajar Aktif, Purata CGPA, Kadar Kelulusan
  - Nilai dikira dinamik dari `dataPelajar`
  - Susun atur 4 kolum responsif (Bootstrap grid)
- **Todo List:**
  1. Bina susun atur 4 kolum menggunakan Bootstrap grid (`col-md-3`)
  2. Reka bentuk setiap kad dengan ikon Bootstrap Icons, nilai besar, dan label
  3. Tulis fungsi `kiraStat()` yang mengira semua nilai KPI dari `dataPelajar`
  4. Paparkan nilai KPI secara dinamik menggunakan `innerHTML`
- **Relevant Context:** Bergantung pada `dataPelajar` dari Sub-Task 2.

---

### Sub-Task 4: Carta Statistik (Chart.js)
- **Status:** `[ ] pending`
- **Intent:** Memaparkan 3 carta visual seperti yang dirancang dalam cadangan reka bentuk.
- **Expected Outcomes:**
  - **Carta 1 (Pie Chart):** Agihan Jantina — Lelaki: 9, Perempuan: 6
  - **Carta 2 (Bar Chart):** Agihan Gred — A (CGPA 3.5–4.0), B (3.0–3.49), C (2.5–2.99), D (2.0–2.49)
  - **Carta 3 (Doughnut Chart):** Status — Aktif: 11, Tidak Aktif: 1, Tangguh: 2 (dikira dari data)
  - Semua carta responsif dan label dalam Bahasa Melayu
- **Todo List:**
  1. Bina susun atur 3 carta menggunakan Bootstrap grid
  2. Tambah elemen `<canvas>` untuk setiap carta
  3. Tulis fungsi `lukisCarta()` yang memproses `dataPelajar` dan merender 3 carta
  4. Tetapkan warna konsisten dan label jelas dalam Bahasa Melayu
- **Relevant Context:** Bergantung pada `dataPelajar` dari Sub-Task 2.

---

### Sub-Task 5: Jadual Pelajar dengan Carian & Penapisan
- **Status:** `[ ] pending`
- **Intent:** Memaparkan senarai lengkap 15 pelajar dalam jadual yang boleh dicari dan ditapis.
- **Expected Outcomes:**
  - Jadual memaparkan 6 kolum: No. Matrik, Nama, Jantina, Semester, CGPA, Status
  - Badge berwarna untuk Status (Aktif = hijau, Tidak Aktif = merah, Tangguh = kuning)
  - Carian nama real-time berfungsi
  - Penapisan semester (Semua / 1 / 2 / 3 / 4) berfungsi
  - Bilangan rekod dipaparkan
- **Todo List:**
  1. Bina bahagian jadual dengan kawalan carian dan dropdown penapisan semester
  2. Tulis fungsi `renderJadual(data)` yang membina HTML jadual dari array data
  3. Tulis fungsi `tapis()` yang menggabungkan carian + penapisan dan memanggil `renderJadual()`
  4. Pasang event listener pada input carian (`oninput`) dan dropdown (`onchange`)
- **Relevant Context:** Bergantung pada `dataPelajar` dari Sub-Task 2.

---

### Sub-Task 6: Footer & Semakan Akhir
- **Status:** `[ ] pending`
- **Intent:** Melengkapkan dashboard dengan footer dan memastikan semua komponen berfungsi dengan betul.
- **Expected Outcomes:**
  - Footer memaparkan nama kolej dan tahun
  - Dashboard responsif pada desktop dan tablet
  - Semua carta dirender dengan betul
  - Carian dan penapisan jadual berfungsi
  - Tiada ralat konsol JavaScript
- **Todo List:**
  1. Tambah `<footer>` dengan maklumat kolej
  2. Semak responsif menggunakan Bootstrap breakpoints
  3. Pastikan semua `<canvas>` carta dirender dengan betul
  4. Uji carian dan penapisan jadual
  5. Semak tiada ralat konsol JavaScript

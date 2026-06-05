# 🚀 Selamat Datang di FASTWorks

## FAST: Financial Analysis & Smart Tracking

**FASTWorks** adalah organisasi GitHub yang digunakan untuk mengelola seluruh pengembangan proyek **FAST (Financial Analysis & Smart Tracking)**. FAST merupakan platform manajemen keuangan berbasis teknologi yang dirancang untuk membantu pengguna mencatat transaksi, menganalisis kondisi keuangan, serta mengelola pengeluaran secara lebih mudah dan terstruktur.

Proyek ini dikembangkan dengan pendekatan modern melalui pemisahan beberapa komponen utama, seperti **frontend**, **backend**, **API service**, serta **AI/Data Science service**. Dengan struktur tersebut, setiap bagian sistem dapat dikembangkan, diuji, dan dikelola secara lebih rapi oleh masing-masing anggota tim.

---

## 📌 Tentang Proyek FAST

FAST dibuat untuk membantu pengguna dalam memahami kondisi keuangan pribadi melalui pencatatan transaksi dan analisis data keuangan. Salah satu fitur utama dari sistem ini adalah kemampuan membaca struk belanja dan mengubahnya menjadi data transaksi yang dapat digunakan untuk kebutuhan pencatatan serta visualisasi keuangan.

Melalui sistem ini, pengguna dapat mengelola transaksi, melihat ringkasan pengeluaran, memantau kondisi keuangan, serta memperoleh informasi yang lebih jelas mengenai pola penggunaan uang. FAST juga mendukung pengembangan fitur berbasis AI untuk membantu proses ekstraksi informasi dari gambar struk belanja.

---

## 🎯 Tujuan Proyek

Tujuan utama dari proyek FAST adalah membangun aplikasi manajemen keuangan yang dapat membantu pengguna dalam mencatat, memantau, dan menganalisis keuangan pribadi secara lebih praktis.

Beberapa tujuan pengembangan FAST antara lain:

- Membantu pengguna mencatat transaksi pemasukan dan pengeluaran.
- Menyediakan dashboard keuangan yang informatif dan mudah dipahami.
- Mengembangkan fitur upload struk untuk mendukung pencatatan transaksi.
- Mengintegrasikan sistem dengan layanan AI untuk proses ekstraksi data struk.
- Menyediakan API backend yang terstruktur dan terdokumentasi.
- Membangun sistem berbasis repository organisasi agar kolaborasi tim lebih rapi.

---

## 📚 Dokumentasi Utama Proyek

Berikut adalah tautan dokumentasi utama yang digunakan dalam proses pengembangan proyek FAST.

### 📄 Project Plan FAST

Dokumen Project Plan berisi penjelasan mengenai latar belakang proyek, tujuan pengembangan, ruang lingkup sistem, pembagian peran, serta rencana pengerjaan proyek.

**Tautan:**  
[Project Plan FAST](https://drive.google.com/file/d/14It28PvqEahSLEqCFheELVlNZXOHfdlK/view?usp=sharing)

---

### 📅 Project Timeline & Master Schedule

Dokumen timeline berisi jadwal pengerjaan proyek, pembagian tugas setiap role, estimasi waktu pengerjaan, serta perkembangan pekerjaan dari setiap minggu.

**Tautan:**  
[Project Timeline & Master Schedule](https://docs.google.com/spreadsheets/d/1p4zBMDv3_BixCXLZQkPSwcF3f4M7LWHYst3qS-99BnM/edit?gid=0#gid=0)

---

### 📑 Software Requirements Specification (SRS)

Dokumen SRS menjelaskan kebutuhan sistem secara lebih detail, baik dari sisi kebutuhan fungsional, kebutuhan non-fungsional, rancangan sistem, hingga spesifikasi teknis yang digunakan dalam pengembangan aplikasi.

**Tautan:**  
[Software Requirements Specification (SRS)](https://drive.google.com/file/d/1TPe2PsL4dN3re9pC7aJaZ0TslmRzbJ2s/view?usp=drive_link)

---

### 🔄 Sequence Diagram FAST

Sequence Diagram digunakan untuk menggambarkan alur komunikasi antar komponen sistem, mulai dari frontend, backend, API, hingga layanan AI.

**Tautan:**  
[Interactive Sequence Diagram](https://hmyid2.github.io/sequence-diagram-fast/)

---

## 🏗️ Struktur Repository FASTWorks

Organisasi FASTWorks terdiri dari beberapa repository yang memiliki fungsi berbeda-beda. Setiap repository dibuat untuk memisahkan bagian pengembangan agar proses kerja tim menjadi lebih terstruktur.

---

## 🌐 Frontend

### fst-frontend

Repository ini digunakan untuk pengembangan tampilan aplikasi FAST. Bagian frontend berfokus pada antarmuka pengguna, halaman login, dashboard, transaksi, visualisasi keuangan, serta fitur upload struk.

**Repository:**  
[fst-frontend](https://github.com/FASTWorks/fst-frontend)

Fitur utama frontend:

- Halaman login dan register.
- Dashboard keuangan.
- Halaman transaksi.
- Visualisasi data keuangan.
- Upload struk belanja.
- Integrasi dengan API backend.
- Tampilan responsif untuk berbagai ukuran layar.

---

## ⚙️ Backend & Microservices

### fst-backend

Repository ini digunakan sebagai pusat pengelolaan backend proyek FAST. Backend berfungsi untuk mengatur proses bisnis, pengelolaan data, autentikasi, transaksi, serta komunikasi dengan layanan lainnya.

**Repository:**  
[fst-backend](https://github.com/FASTWorks/fst-backend)

---

### fst-gateway-service

Repository ini digunakan sebagai API Gateway. API Gateway berfungsi sebagai pintu utama yang menerima request dari frontend, lalu meneruskannya ke service yang sesuai.

**Repository:**  
[fst-gateway-service](https://github.com/FASTWorks/fst-gateway-service)

Fungsi utama:

- Mengatur routing request.
- Menghubungkan frontend dengan backend services.
- Menjadi jalur utama komunikasi API.
- Menyediakan dokumentasi API melalui endpoint `/api-docs`.

---

### fst-auth-service

Repository ini digunakan untuk mengelola autentikasi pengguna, seperti register, login, verifikasi akun, dan validasi token.

**Repository:**  
[fst-auth-service](https://github.com/FASTWorks/fst-auth-service)

Fungsi utama:

- Register pengguna.
- Login pengguna.
- Verifikasi akun.
- Pengelolaan token JWT.
- Validasi akses pengguna.

---

### fst-finance-service

Repository ini digunakan untuk mengelola data keuangan pengguna, seperti pemasukan, pengeluaran, kategori transaksi, dan data transaksi lainnya.

**Repository:**  
[fst-finance-service](https://github.com/FASTWorks/fst-finance-service)

Fungsi utama:

- Mencatat transaksi keuangan.
- Mengelola data pemasukan dan pengeluaran.
- Mengelola kategori transaksi.
- Menyediakan data keuangan untuk kebutuhan dashboard.

---

### fst-analytics-service

Repository ini digunakan untuk melakukan proses analisis data keuangan pengguna. Service ini berfungsi untuk menghasilkan ringkasan, insight, dan visualisasi yang dapat membantu pengguna memahami kondisi keuangan mereka.

**Repository:**  
[fst-analytics-service](https://github.com/FASTWorks/fst-analytics-service)

Fungsi utama:

- Menghitung ringkasan keuangan.
- Menganalisis pola pengeluaran.
- Menyediakan data insight keuangan.
- Mendukung visualisasi pada dashboard frontend.

---

### fst-aggregator-service

Repository ini digunakan untuk menggabungkan data dari beberapa service agar frontend dapat menerima data yang sudah siap ditampilkan.

**Repository:**  
[fst-aggregator-service](https://github.com/FASTWorks/fst-aggregator-service)

Fungsi utama:

- Mengambil data dari beberapa service.
- Menggabungkan data untuk kebutuhan dashboard.
- Mengurangi kompleksitas request dari frontend.
- Menyediakan data yang lebih terstruktur untuk tampilan aplikasi.

---

## 🧠 AI & Data Science

### fst-ai-service

Repository ini digunakan untuk layanan AI yang berfungsi memproses gambar struk belanja. Service ini mendukung proses OCR atau ekstraksi informasi dari struk agar dapat digunakan sebagai data transaksi.

**Repository:**  
[fst-ai-service](https://github.com/FASTWorks/fst-ai-service)

Fungsi utama:

- Memproses gambar struk belanja.
- Melakukan ekstraksi informasi dari struk.
- Menghasilkan data transaksi dari hasil pembacaan struk.
- Menghubungkan sistem backend dengan model AI.

---

### fst-data-science

Repository ini digunakan untuk eksplorasi data, analisis dataset, proses preprocessing, serta pengembangan awal model berbasis data.

**Repository:**  
[fst-data-science](https://github.com/FASTWorks/fst-data-science)

Fungsi utama:

- Data gathering.
- Data preparation.
- Exploratory Data Analysis.
- Visualisasi data.
- Preprocessing dataset.
- Eksperimen data untuk kebutuhan AI.

---

### fst-ai-engineer

Repository ini digunakan untuk proses pengembangan model AI, mulai dari training, testing, evaluasi performa, hingga export model.

**Repository:**  
[fst-ai-engineer](https://github.com/FASTWorks/fst-ai-engineer)

Fungsi utama:

- Training model.
- Testing model.
- Evaluasi performa model.
- Export model.
- Pengembangan pipeline inference.

---

## 🗺️ Arsitektur Sistem FAST

FAST dikembangkan dengan pendekatan modular agar setiap bagian sistem dapat berjalan secara lebih terstruktur. Frontend berperan sebagai antarmuka pengguna, backend mengelola proses bisnis dan data, sedangkan layanan AI digunakan untuk mendukung proses ekstraksi informasi dari struk belanja.

Berikut gambaran umum arsitektur sistem FAST:

```mermaid
graph TD
    Client[Frontend FAST] --> Gateway[API Gateway Service]

    Gateway --> Auth[Auth Service]
    Gateway --> Finance[Finance Service]
    Gateway --> Analytics[Analytics Service]
    Gateway --> Aggregator[Aggregator Service]

    Aggregator --> Auth
    Aggregator --> Finance
    Aggregator --> Analytics

    Finance --> AI[AI Service]
    AI --> Model[AI Model / OCR Processing]

    Finance --> Database[(Database)]
    Auth --> Database
    Analytics --> Database

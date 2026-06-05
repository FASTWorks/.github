# 🚀 Selamat Datang di FASTWorks (Financial AI System Tracker)

**FASTWorks** adalah organisasi di balik pengembangan **FAST**, sebuah platform manajemen keuangan generasi baru yang ditenagai oleh Kecerdasan Buatan (AI) dan dibangun di atas arsitektur *Microservices* modern. 

Misi kami adalah membantu pengguna melacak, menganalisis, dan mengoptimalkan kesehatan finansial mereka secara otomatis melalui fitur mutakhir seperti *AI Receipt Parsing* (pembacaan struk otomatis), kalkulasi *Cashflow*, dan peringatan dini pembengkakan pengeluaran (*Burn Rate*).

---

## 🏗️ Gambaran Ekosistem & Repositori

Ekosistem FASTWorks terdiri dari berbagai repositori yang saling terintegrasi, mulai dari antarmuka pengguna, layanan *backend*, hingga lab eksperimen AI.

### 🌐 Antarmuka Pengguna (Client-Side)
* 💻 **[fst-frontend](https://github.com/FASTWorks/fst-frontend)**: Aplikasi antarmuka utama (UI/UX) yang digunakan oleh klien untuk berinteraksi dengan dasbor keuangan.

### ⚙️ Mesin Utama (Backend & Microservices)
* 📦 **[fst-backend](https://github.com/FASTWorks/fst-backend)**: Repositori utama (*Superproject / Monorepo*) yang mengorkestrasi dan menyatukan seluruh layanan *backend*.
* 🚪 **[fst-gateway-service](https://github.com/FASTWorks/fst-gateway-service)**: Gerbang API (*API Gateway*) yang menangani *routing* permintaan dari *frontend* dan kebijakan *load balancing*.
* 🔐 **[fst-auth-service](https://github.com/FASTWorks/fst-auth-service)**: Layanan terpusat untuk autentikasi, manajemen pengguna, verifikasi OTP, dan validasi token JWT.
* 💰 **[fst-finance-service](https://github.com/FASTWorks/fst-finance-service)**: Inti pengelola keuangan yang mencatat arus kas, alokasi *budget*, serta target tabungan pengguna.
* 📊 **[fst-analytics-service](https://github.com/FASTWorks/fst-analytics-service)**: Mesin komputasi statistik untuk menghitung Skor Kesehatan Finansial (*Financial Health Score*) dan peringatan pengeluaran.
* 📈 **[fst-aggregator-service](https://github.com/FASTWorks/fst-aggregator-service)**: Penggabung data (*Aggregator*) dari berbagai *service* untuk merender Dasbor *Frontend* secepat kilat.

### 🧠 Kecerdasan Buatan (AI & Data Science)
* 🤖 **[fst-ai-service](https://github.com/FASTWorks/fst-ai-service)**: Layanan AI level produksi (Python/FastAPI) untuk memproses gambar struk belanja (*OCR*) dan memprediksi kategori pengeluaran.
* 🧪 **[fst-data-science](https://github.com/FASTWorks/fst-data-science)**: Ruang kerja berbasis *Jupyter Notebook* untuk eksperimen data, analisis, dan permodelan data finansial mentah.
* 🛠️ **[fst-ai-engineer](https://github.com/FASTWorks/fst-ai-engineer)**: Repositori khusus pelatihan (*training*), evaluasi, dan rekayasa model *Machine Learning* sebelum di-*deploy* ke produksi.

---

## 🗺️ Arsitektur Microservices FAST Backend

Arsitektur kami dirancang untuk *scalability* tingkat tinggi. Setiap permintaan dari pengguna akan melewati **Gateway**, yang kemudian didistribusikan ke layanan-layanan spesifik yang berjalan secara independen.

Berikut adalah diagram alir data (*Data Flow*) dari sistem kami:

```mermaid
graph TD
    Client[Frontend / Client App] -->|HTTP Requests| Gateway[API Gateway Service]
    
    Gateway -->|Routing & Proxy| Auth[Auth Service]
    Gateway -->|Routing & Proxy| Finance[Finance Service]
    Gateway -->|Routing & Proxy| Analytics[Analytics Service]
    Gateway -->|Routing & Proxy| Aggregator[Aggregator Service]
    
    Aggregator -->|Internal Call| Auth
    Aggregator -->|Internal Call| Analytics
    Aggregator -->|Internal Call| Finance
    
    Finance -->|OCR Analysis| AI[AI Service]
    Analytics -->|Financial Insight| AI
    
    classDef default fill:#ffffff,stroke:#000000,stroke-width:2px,color:#000000;
    classDef gateway fill:#ffffff,stroke:#000000,stroke-width:4px,color:#000000;
    
    class Gateway gateway;

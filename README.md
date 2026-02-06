# WA-Web-Optimizer

## Optimisasi WhatsApp Web (Aman)

WA-Web-Optimizer adalah skrip PowerShell portable untuk optimisasi WhatsApp Web di semua browser utama.  
Dirancang aman, tanpa logout, tanpa menutup browser, dan cocok dijalankan otomatis.

---

## 🎯 Tujuan
- Menjaga performa WhatsApp Web tetap stabil
- Optimisasi ringan dan aman
- Tidak mengganggu sesi login atau aktivitas pengguna

---

## ✅ Yang Dilakukan Skrip
- Membersihkan cache runtime ringan:
  - GPUCache
  - Code Cache
- Mendeteksi semua profil browser
- Mendukung browser:
  - Google Chrome
  - Microsoft Edge
  - Brave Browser
  - Opera
  - Mozilla Firefox

---

## ❌ Yang TIDAK Dilakukan
- Tidak logout WhatsApp Web
- Tidak menutup browser
- Tidak menghapus Cookies
- Tidak menghapus Local Storage
- Tidak menghapus IndexedDB
- Tidak menghapus data chat

Skrip ini **hanya optimisasi runtime**, bukan pembersihan agresif.

---

## 📂 Area yang Dibersihkan
Hanya folder berikut:
- GPUCache
- Code Cache

Folder autentikasi **tidak disentuh**.

---

## ⬇️ Download Script

https://github.com/ncexs/WA-Web-Runtime-Optimizer/releases/download/1.0/WA-Web-Runtime-Optimizer.ps1

---

## ▶️ Cara Menjalankan Manual
1. Klik kanan `WA-Web-Runtime-Optimizer.ps1`
2. Pilih **Run with PowerShell**
3. Tunggu proses selesai
4. Tidak perlu refresh WhatsApp Web

---

## ⏱️ Setup Otomatis (Task Scheduler – Setiap 1 Jam)

### 1️⃣ Buka Task Scheduler
Tekan **Win + R**, lalu ketik:
```
taskschd.msc
```
Tekan **Enter**

---

### 2️⃣ Buat Task Baru
Klik **Create Task** (jangan pilih *Basic Task*)

**Tab General**
- Name:
  ```
  WA Web Runtime Optimizer
  ```
- Centang:
  - Run whether user is logged on or not
  - Run with highest privileges

---

### 3️⃣ Tab Triggers
- Klik **New**
- Begin the task: **On a schedule**
- Pilih **Daily**
- Advanced settings:
  - Repeat task every: **1 hour**
  - For a duration of: **Indefinitely**
- Centang **enable**
- Klik **OK**

---

### 4️⃣ Tab Actions
- Klik **New**
- Action: **Start a program**
- Program/script:
  ```
  powershell.exe
  ```
- Add arguments:
  ```
  -ExecutionPolicy Bypass -File "C:\Users\ncexs\Downloads\WA-Web-Runtime-Optimizer.ps1"
  ```
- Start in (optional) :
  ```
  C:\Users\ncexs\Downloads\WA-Web-Runtime-Optimizer.ps1

- Ganti `C:\Users\ncexs\Downloads\` sesuai lokasi kamu menyimpan script 

---

### 5️⃣ Tab Conditions
- Hilangkan centang:
  - Start the task only if the computer is on AC power

---

### 6️⃣ Tab Settings
- Centang:
  - Allow task to be run on demand
  - Run task as soon as possible after a scheduled start is missed
- Jangan centang:
  - Stop the task if it runs longer than

Klik **OK** dan masukkan password Windows jika diminta.

---

## 🔁 Tentang Refresh
- Skrip **tidak melakukan refresh**
- Refresh manual **tidak wajib**
- Untuk mode otomatis 1 jam:
  - Biarkan berjalan di background

---

## 🧠 Prinsip Desain
- Aman > agresif
- Stabilitas jangka panjang
- Tidak mengganggu sesi WA Web

---

## 📄 Lisensi
Bebas digunakan dan dimodifikasi untuk kebutuhan pribadi atau internal

# Baby 1 : Reverse search engine
# 📸 Reverse Search Engine — Deep Dive Versi Gama

> 🚀 Sebuah asisten pintar yang membantu mahasiswa dari *screenshot tugas* menuju *konsep, referensi, dan petunjuk step-by-step* yang dibutuhkan — bukan sekadar jawaban mentah.

---

## 🎯 Konsep Utama

Alih-alih memberikan jawaban langsung, sistem ini memprediksi *materi apa yang kamu perlukan* dari sebuah screenshot:

- Upload soal matematika → sistem akan bilang:  
  “Ini pakai konsep limit.”  
  “Rumus turunan yang kamu butuhkan: …”  
  “Pelajari dulu materi ini.”  
  “Ini referensi video + latihan soal.”

Seperti punya *guru privat digital* yang mengarahkan dengan lembut.

---

## ⭐ Fitur Utama

1. *OCR + Pemahaman Konteks*  
   - Ekstrak teks dari screenshot (matematika, coding, fisika, essay, diagram).  
   - Klasifikasi otomatis sesuai jenis tugas.

2. *Engine “Kamu Butuh Apa?”*  
   - Prediksi rumus, teori, bab materi, tools, atau library yang relevan.  

3. *Saran Latihan Pendukung*  
   - Jika soal turunan lanjut → sistem menyarankan latihan turunan dasar terlebih dahulu.  

4. *Generator Referensi Otomatis*  
   - Memberikan link YouTube, PDF, artikel, dan latihan soal (via API resmi).  

5. *Mode Step-by-Step Hint*  
   - Memberikan petunjuk kecil, bukan jawaban penuh.  
   - Contoh: “Coba cek pola angkanya, mirip tugas minggu lalu 😉”  

6. *AI Difficulty Estimator*  
   - Menilai tingkat kesulitan soal (1–10).  
   - Memberikan motivasi: “Soal ini lumayan susah, tapi kamu pasti bisa!”  

---

## 🧠 Arsitektur Sistem (Sederhana)

1. *Input Layer* → Upload screenshot → konversi ke base64  
2. *OCR Engine* → Tesseract / EasyOCR / Google Vision API  
3. *NLP + Context Analyzer* → klasifikasi, intent detector, keyword extraction  
4. *Knowledge Mapper* → mapping soal → bab → rumus → konsep  
5. *Recommendation Engine* → mencari referensi (video, artikel, latihan)  
6. *Output Builder* → hasil akhir berupa panduan belajar  

---

## 🛠 Teknologi yang Digunakan

### Frontend
- *React.js* (Web)  
- *React Native* (Mobile)  
- UI Libraries: Material UI, Shadcn, Chakra  

### Backend
- *Node.js* (Express.js / NestJS)  
- Alternatif: Python (FastAPI)  

### AI/NLP
- *spaCy, **Transformers (BERT, RoBERTa)*  
- *Sentence similarity models*  
- *Tesseract OCR*  

### Database
- *MongoDB / PostgreSQL*  
- Menyimpan mapping bab → rumus → referensi  

---


## 🚀 Cara Menjalankan

### Prasyarat
- Node.js v18+  
- Python 3.9+ (opsional untuk backend FastAPI)  
- MongoDB/PostgreSQL  

### Instalasi
```bash
# Clone repo
git clone https://github.com/username/reverse-search-engine.git
cd reverse-search-engine

# Install dependencies
npm install   # frontend/backend JS
pip install -r requirements.txt   # backend Python (opsional)

# Jalankan development
npm run dev   # frontend
npm run start # backend

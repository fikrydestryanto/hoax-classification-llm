# hoax-classification-llm
 
# 🧠 Hoax Classification using LLM-Based Model  
**Author:** Fikry Destryanto  

---

### ● Title Project  
**Hoax Classification using LLM-Based Model**

---

### ● Project Overview  
Proyek ini bertujuan untuk mengklasifikasikan berita politik Indonesia menjadi dua kategori utama:  
- **HOAX** → Berita yang mengandung misinformasi atau klaim palsu.  
- **FACT** → Berita yang berdasarkan informasi terverifikasi.  

Pendekatan yang digunakan adalah **LLM-Based Prompt Classification**, di mana model *Large Language Model (LLM)* diberi instruksi (*prompt*) untuk menganalisis teks berita dan menentukan klasifikasinya.  
Model berjalan melalui **Replicate API**, yang mengeksekusi model AI untuk membaca konteks berita, memahami instruksi, dan menghasilkan prediksi berupa kata “HOAX” atau “FACT”.  

---

### ● Raw Dataset Link  
Dataset yang digunakan merupakan kumpulan berita politik Indonesia dari tahun 2019–2024 yang telah dibersihkan.  
Sumber dataset:  
🔗 [Indonesian Fact and Hoax Political News – Kaggle](https://www.kaggle.com/datasets/linkgish/indonesian-fact-and-hoax-political-news)

---

### ● Insight & Findings  
- Teks berita dengan gaya bahasa **sensasional dan emosional** cenderung dikategorikan sebagai *HOAX*.  
- Berita yang menggunakan **bahasa formal, memiliki sumber jelas, dan struktur kalimat yang faktual** lebih sering dikategorikan sebagai *FACT*.  
- Model LLM mampu memahami konteks politik Indonesia dengan cukup baik melalui prompt berbahasa Inggris yang deskriptif.  
- Pendekatan *prompt-based classification* mempercepat proses pelabelan otomatis dibandingkan anotasi manual.  
- Proses labeling dilakukan secara bertahap dengan jeda antar permintaan (`time.sleep(10)`) untuk menghindari batasan API (rate limit).

---

### ● AI Support Explanation  
- **Pendekatan yang digunakan:** *Prompt-Based Classification (LLM Inference)*  
- **Platform AI:** Replicate API  
- **Fungsi utama:**  
  - `output.invoke(prompt)` → Mengirim instruksi ke model AI untuk menghasilkan label *HOAX* atau *FACT*.  
  - `time.sleep(10)` → Memberi jeda setiap permintaan untuk menjaga stabilitas proses.  
- **Kelebihan pendekatan ini:**  
  - Tidak memerlukan dataset berlabel.  
  - Memanfaatkan kemampuan pemahaman konteks model LLM.  
  - Dapat digunakan untuk analisis cepat dan skala besar.  

---


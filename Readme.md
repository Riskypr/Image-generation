# 🎨 Stable Diffusion Image Generation & Manipulation Pipeline

Repository ini berisi implementasi lengkap pipeline *Generative AI* menggunakan **Stable Diffusion v1.5** untuk berbagai tugas computer vision, meliputi:

- Text-to-Image Generation
- Hyperparameter Exploration (Guidance Scale & Inference Steps)
- Batch Image Generation
- Scheduler Comparison
- Image-to-Image Refinement
- Inpainting (Manual & Automatic Masking)
- Outpainting & Image Expansion
- Zoom-out Multi-step Generation

Proyek ini dibuat menggunakan **PyTorch + Hugging Face Diffusers** dan dijalankan di Google Colab dengan GPU support.

---

# 🚀 Features

## 1. 🧠 Text-to-Image Generation
Menghasilkan gambar dari deskripsi teks menggunakan Stable Diffusion.

### Fitur:
- Simple generation
- Advanced generation (custom guidance scale & inference steps)
- Negative prompt support

---

## 2. ⚙️ Hyperparameter Analysis

### 🔹 Guidance Scale
Menganalisis pengaruh guidance scale terhadap hasil gambar:
- Scale rendah → lebih natural & detail bebas
- Scale tinggi → lebih sesuai prompt & lebih terstruktur

### 🔹 Inference Steps
Menganalisis jumlah langkah denoising:
- Steps rendah → noise tinggi, detail kurang
- Steps tinggi → gambar lebih halus & stabil

---

## 3. 📦 Batch Generation
Generate beberapa gambar sekaligus dari satu prompt untuk eksplorasi variasi output.

---

## 4. 🔄 Scheduler Comparison
Membandingkan hasil dari berbagai scheduler:
- Euler A
- DPM++
- DDIM

Setiap scheduler memberikan karakteristik visual yang berbeda dalam:
- detail
- stabilitas
- style rendering

---

## 5. 🖼️ Image-to-Image (Refinement)
Menyempurnakan gambar awal menggunakan pipeline img2img:
- mempertahankan struktur awal
- meningkatkan detail & kualitas visual

---

## 6. 🎭 Inpainting

### 🔹 Manual Masking
Mengedit bagian tertentu dari gambar menggunakan mask buatan manual.

### 🔹 Automatic Masking (Segmentation)
Menggunakan model segmentasi untuk membuat mask otomatis.

---

## 7. 🌌 Outpainting
Memperluas canvas gambar ke arah tertentu (top/right/bottom/left) dan mengisi area kosong dengan AI-generated content.

---

## 8. 🔍 Zoom Out Generation
Membuat efek zoom-out bertahap dengan:
- iterative outpainting
- multi-step inpainting

---

# 🛠️ Installation

```bash
pip install diffusers transformers accelerate safetensors
pip install opencv-python pillow matplotlib

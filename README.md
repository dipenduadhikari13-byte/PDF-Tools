# 📄 PDF Tools — Fast, Local, No-Nonsense

A lightweight, high-performance PDF utility suite built with Streamlit.

No uploads to external servers. No unnecessary bloat. Just fast, practical tools.

---

## ⚡ Features

### 📉 PDF Compressor

* Dual engine:

  * **Ghostscript (high compression)**
  * **pypdf fallback (pure Python)**
* Smart iterative compression (DPI + quality tuning)
* Prevents file size increase (edge-case safe)
* Metadata cleanup support

---

### ✂️ PDF Splitter & Extractor

* Extract pages with flexible syntax:

  * `1-3`, `1,5,8`, `last3`, `odd`, `even`
* Reverse ranges supported (`7-3`)
* Split by:

  * custom ranges
  * fixed page intervals
  * equal parts
* Lossless processing (no quality loss)

---

## 🧠 Design Philosophy

* 🔒 Local-first (no file leaves your system)
* ⚡ Fast startup (minimal dependencies)
* 🧩 Modular architecture
* 🛡️ Safe fallback mechanisms

---

## 📦 Installation

### 1. Clone repo

```bash
git clone https://github.com/dipenduadhikari13-byte/PDF-Tools.git
cd PDF-Tools
```

---

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

---

### 3. (Optional but recommended) Install Ghostscript

#### Linux (Arch)

```bash
sudo pacman -S ghostscript
```

#### Debian / Ubuntu (used by Streamlit Cloud)

```bash
sudo apt install ghostscript
```

---

### 4. Run app

```bash
streamlit run app.py
```

---

## ☁️ Deployment (Streamlit Cloud)

This repo includes:

* `requirements.txt` → Python dependencies
* `packages.txt` → installs Ghostscript automatically

👉 Works out-of-the-box on Streamlit Community Cloud

---

## ⚠️ Notes

* Ghostscript greatly improves compression quality
* Large PDFs (>100MB) may hit memory limits on cloud
* Fallback mode ensures functionality without Ghostscript

---

## 🧩 Architecture

```text
app.py
pages/
 ├── pdf_resizer.py
 ├── pdf_splitter.py
```

---

## 🚀 Future Plans

* Batch processing
* CLI version
* Drag & drop multi-file support
* Advanced optimization profiles

---

## 📜 License

MIT License

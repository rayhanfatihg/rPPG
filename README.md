# Real-time rPPG Pipeline

Proyek ini mengimplementasikan sistem remote Photoplethysmography (rPPG) waktu nyata menggunakan webcam. Sistem ini mendeteksi wajah, mengekstrak sinyal warna dari area kulit (pipi dan dahi), dan menggunakan algoritma POS (Plane-Orthogonal-to-Skin) untuk mengestimasi detak jantung (BPM).

## Pembeda dari demo di kelas
- Menggunakan area spesifik seperti pipi dan jidat untuk mengurangi noise dengan menggunakan mediapipe untuk trackingnya
- Menggunakan metode POS yang lebih robust
- Menggunakan filter lowcut = 0.7 dan highcut = 4.0 dengan fs adaptif
- Menambah visualisasi Real-time signal plotting, Frequency Spectrum, dan BPM display.

## Fitur

- **Deteksi Wajah**: Menggunakan MediaPipe Face Mesh.
- **Ekstraksi Sinyal**: Algoritma POS yang tahan terhadap gerakan ringan.
- **ROI Cerdas**: Mengambil sinyal dari area pipi dan dahi.
- **Visualisasi**: Grafik sinyal detak jantung dan spektrum frekuensi secara real-time.

## Persyaratan Sistem

- Python 3.7 atau lebih baru
- Webcam

## Cara Menjalankan

1.  **Instalasi Dependensi**
    Pastikan Anda telah menginstal semua library yang dibutuhkan. Jalankan perintah berikut di terminal:

    ```bash
    pip install -r requirements.txt
    ```

2.  **Jalankan Program**
    Buka file `rPPG.ipynb` menggunakan Jupyter Notebook atau VS Code.
    Jalankan semua cell secara berurutan. Cell terakhir akan membuka jendela kamera.

3.  **Penggunaan**
    - Pastikan wajah Anda terlihat jelas di kamera dengan pencahayaan yang cukup.
    - Tunggu beberapa detik agar sinyal stabil.
    - Grafik hijau menunjukkan sinyal detak jantung.
    - Grafik magenta menunjukkan spektrum frekuensi.
    - Tekan tombol `ESC` pada keyboard untuk keluar dari program.

## Struktur File

- `rPPG.ipynb`: Kode utama program (Jupyter Notebook).
- `requirements.txt`: Daftar library yang dibutuhkan.
- `README.md`: Dokumentasi proyek.



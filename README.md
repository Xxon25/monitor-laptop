# Dual-View HDMI Viewer 🖥️⚡

Dual-View HDMI Viewer adalah aplikasi berbasis Windows (executable) ringan yang mengubah laptop kedua Anda menjadi monitor eksternal untuk laptop utama melalui koneksi HDMI (via capture card/kabel HDMI to USB). Dibangun untuk latensi ultra-rendah dan pengalaman _seamless_ layaknya monitor asli.

![Logo](file:///C:/Users/zonaa/.gemini/antigravity/brain/9ba8620f-9080-4138-bdaa-5f338677a1cb/dual_view_logo_1778399498089.png)

## 🚀 Fitur Utama (Tugas 1: Bug Fix & Optimization)
- **Ultra-Low Latency:** Menggunakan backend DirectShow (`CAP_DSHOW`), format dekompresi MJPG, dan buffer minimal (`BUFFERSIZE=1`) untuk menekan *delay* serendah mungkin.
- **Auto-Resolution Detect:** Secara otomatis mendeteksi dan menyesuaikan resolusi maksimal (720p/1080p) dan frame rate optimal dari hardware.
- **Toggle Fullscreen:** Mode layar penuh tanpa border, memberikan ilusi monitor kedua sesungguhnya (Tekan `F`).
- **Always on Top:** Jaga jendela proyeksi tetap melayang di atas aplikasi lain (Tekan `T`).
- **Auto-Recovery (Error Handling):** Penanganan error cerdas ketika kabel HDMI tercabut. Menampilkan peringatan "NO SIGNAL" dan akan terus me-refresh hingga sinyal terhubung kembali.

## 🛠️ Teknologi yang Digunakan
- **Python 3.x:** Bahasa pemrograman backend untuk pengembangan yang efisien dan dapat di-*compile* menjadi standalone `.exe`.
- **OpenCV (`cv2`):** Core engine rendering yang bertugas menangkap frame RAW dari input HDMI dan menampilkannya dengan akselerasi yang tepat.
- **NumPy:** Membantu dalam _matrix generation_ (digunakan saat mem-build UI error screen secara dinamis).

## 📥 Cara Instalasi

install aplikasi di laptop yang mau dijadikan monitor kedua 
https://www.mediafire.com/file/q75o4k1v8xyqbjc/HDMI_Viewer.exe/file

### Prasyarat Perangkat Keras:
- Laptop 1 (Sebagai Sumber / Monitor Utama)
- Laptop 2 (Sebagai Layar Tambahan)
- *HDMI Video Capture Card* (Konektor USB ke HDMI) + Kabel HDMI.

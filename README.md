# Tema Kibaran-X: Migrasi ke PHP 8.2

Repositori ini digunakan untuk proses audit dan perbaikan tema WordPress **Kibaran** agar kompatibel dengan standar **PHP 8.2**. Proses pengembangan dilakukan menggunakan **Project IDX Google** dengan bantuan **Gemini AI**.

### 🛠️ Fokus Perbaikan
* **Standardisasi Class**: Mengubah constructor lama menjadi `public function __construct()` untuk menghindari error pada PHP 8.2.
* **Dynamic Properties**: Menangani peringatan *deprecated* dengan mendeklarasikan properti secara eksplisit atau menggunakan atribut `#[AllowDynamicProperties]`.
* **Optimasi Query**: Mempercepat loading berita dengan parameter `no_found_rows` pada `WP_Query`.
* **Caching**: Implementasi *Transient API* untuk mengurangi beban database tanpa menggunakan plugin tambahan.

### 🚀 Panduan Pengembangan di IDX
1. **Ekstrak File**: Gunakan terminal untuk membongkar file ZIP tema agar bisa diedit:
   ```bash
   unzip kibaran-x.zip

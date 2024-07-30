# 🖼️🎵 Manipulasi Gambar dan Audio

## 🖼️ Manipulasi Gambar dengan Pillow

### 🔍 Dasar-dasar Pillow

Pillow adalah pustaka Python yang digunakan untuk memanipulasi gambar. Ini memungkinkan kita untuk memuat, memanipulasi, dan menyimpan gambar dalam berbagai format.

### 💾 Instalasi Pillow

Gunakan perintah berikut untuk menginstal Pillow:

```bash
pip(windows)/pip3(linux) install pillow
```

### 🖼️ Memuat dan Menyimpan Gambar

Contoh kode untuk memuat dan menyimpan gambar:

```python
from PIL import Image

# Memuat gambar
image = Image.open('example.jpg')

# Menyimpan gambar
image.save('result.jpg')
```

Penjelasan:

- Menggunakan `Image.open` untuk memuat gambar.
- Menggunakan `image.save` untuk menyimpan gambar yang telah dimuat.

### ✂️ Operasi Dasar

#### Cropping

```python
cropped_image = image.crop((10, 10, 200, 200))
cropped_image.save('cropped_result.jpg')
```

Penjelasan:

- `image.crop` digunakan untuk memotong gambar dengan koordinat yang diberikan.

#### Resizing

```python
resized_image = cropped_image.resize((100, 100))
resized_image.save('resized_result.jpg')
```

Penjelasan:

- `image.resize` digunakan untuk mengubah ukuran gambar.

#### Filtering

```python
from PIL import ImageFilter

filtered_image = resized_image.filter(ImageFilter.BLUR)
filtered_image.save('filtered_result.jpg')
```

Penjelasan:

- `image.filter` digunakan untuk menerapkan filter ke gambar.

## 🎵 Manipulasi Audio dengan Pydub

### 🔍 Dasar-dasar Pydub

Pydub adalah pustaka Python yang digunakan untuk memanipulasi file audio. Ini memungkinkan kita untuk memuat, memanipulasi, dan menyimpan file audio dalam berbagai format.

### 💾 Instalasi Pydub

Gunakan perintah berikut untuk menginstal Pydub:

```bash
pip(windows)/pip3(linux) install pydub
```

### 🎵 Memuat dan Menyimpan File Audio

Contoh kode untuk memuat dan menyimpan file audio:

```python
from pydub import AudioSegment

# Memuat file audio
audio = AudioSegment.from_file('example.mp3')

# Menyimpan file audio
audio.export('result.mp3', format='mp3')
```

Penjelasan:

- Menggunakan `AudioSegment.from_file` untuk memuat file audio.
- Menggunakan `audio.export` untuk menyimpan file audio yang telah dimuat.

### ✂️ Operasi Dasar

#### Pemotongan

```python
clipped_audio = audio[:10000]  # Mendapatkan 10 detik pertama
clipped_audio.export('clipped_result.mp3', format='mp3')
```

Penjelasan:

- Memotong file audio untuk mendapatkan 10 detik pertama.

#### Penggabungan

```python
combined_audio = audio + clipped_audio
combined_audio.export('combined_result.mp3', format='mp3')
```

Penjelasan:

- Menggabungkan dua file audio.

#### Konversi Format

```python
audio.export('result.wav', format='wav')
```

Penjelasan:

- Mengonversi file audio ke format lain.

#### Pengaturan Volume

```python
louder_audio = audio + 10  # Meningkatkan volume sebesar 10dB
louder_audio.export('louder_result.mp3', format='mp3')
```

Penjelasan:

- Meningkatkan volume audio sebesar 10dB.

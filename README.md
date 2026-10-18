# MangaBrush Translator

**Generative Fill & Comic Translator** — web app single-page untuk menerjemahkan halaman manga/komik langsung di browser.

## Cara pakai
1. Upload halaman manga, atau pakai contoh komik bawaan (otomatis dimuat).
2. Pilih **Brush Mask**, sapukan kuas merah di atas teks asing (balon kata / SFX).
3. Klik **✨ Translate Brushed Area** — area dibersihkan (inpainting) dan diisi teks Bahasa Indonesia bergaya komik tepat di tengah area brush.
4. Klik teks hasil untuk menggeser/memutar, klik 2× untuk edit. Atur font, ukuran, warna & outline di panel Properties.
5. **Export / Download Hasil (PNG)** untuk mengunduh halaman pada resolusi asli.

## Mode AI
- **Mode Demo (default):** tanpa API key — simulasi pintar: area di-brush dibersihkan dan diisi contoh dialog/SFX Bahasa Indonesia.
- **Mode API asli:** isi Gemini Vision API Key di *Settings AI* → potongan area brush dikirim ke Gemini untuk OCR + terjemahan asli (Jepang/Korea/Mandarin/Inggris → Indonesia).

## Fitur
- Brush mask merah semi-transparan, ukuran kuas 10–100px, eraser per-mask, undo (Ctrl+Z), clear all
- Sapuan berdekatan otomatis digabung jadi satu region/balon
- Inpainting: Bubble Mode (isi putih bersih mengikuti bentuk balon) & SFX/Background Redraw (patch tekstur)
- Auto-typesetting: huruf kapital komik, rata tengah, auto word-wrap, outline putih, font otomatis menyesuaikan area
- Zoom (scroll) & pan, riwayat terjemahan (teks asli vs terjemahan), export PNG resolusi asli

Dibangun dengan HTML5 + Tailwind CSS + Fabric.js dalam satu file `index.html`.

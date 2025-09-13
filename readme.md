# 🍗 Ayam Crispy Terenak - Panduan Website

Panduan lengkap untuk website bisnis ayam crispy dengan desain responsif dan fitur pemesanan online.

## 📋 Gambaran Umum

Website ini dirancang untuk bisnis kuliner ayam crispy dengan fokus pada:
- Menampilkan menu andalan
- Menerima pesanan melalui WhatsApp
- Menampilkan testimoni pelanggan
- Memberikan informasi kontak dan lokasi

## 🎨 Fitur Desain

- **Design Modern**: Menggunakan kombinasi warna kuning (primary) dan merah (secondary)
- **Responsif**: Bekerja optimal di desktop, tablet, dan mobile
- **Interaktif**: Animasi hover, efek transisi, dan navigasi smooth
- **User-Friendly**: Tampilan bersih dan mudah dinavigasi

## 🛠️ Teknologi yang Digunakan

- **HTML5** - Struktur website
- **Tailwind CSS** - Framework styling
- **Font Awesome** - Ikon
- **Google Fonts** - Font Poppins
- **Google Maps** - Embed peta lokasi

## 📱 Sections Website

1. **Navigation Bar** - Menu navigasi sticky dengan logo
2. **Hero Section** - Gambar header dengan CTA utama
3. **Keunggulan** - Fitur unggulan bisnis
4. **Menu** - Daftar menu ayam crispy dengan harga
5. **Tentang** - Informasi tentang bisnis
6. **Testimoni** - Ulasan dari pelanggan
7. **Kontak** - Informasi kontak dan peta lokasi
8. **Footer** - Informasi tambahan dan link sosial media

## ⚙️ Konfigurasi

### 1. Informasi Bisnis

Ubah informasi berikut di dalam tag `<script>` di bagian Structured Data dan konten website:

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "Restaurant",
  "name": "Ayam Crispy Terenak",
  "image": "https://images.unsplash.com/photo-1562967914-608f82629710?auto=format&fit=crop&w=1200&q=80",
  "description": "Ayam crispy dengan bumbu rahasia turun temurun...",
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "Jl. Raya Kuliner No. 123",
    "addressLocality": "Jakarta",
    "addressRegion": "DKI Jakarta",
    "postalCode": "12345"
  },
  "telephone": "+6281234567890",
  "priceRange": "Rp 15.000 - Rp 50.000"
}
</script>
```

### 2. Informasi Kontak

Ganti informasi kontak di berbagai section:

```html
<!-- Di navigation -->
<a href="https://wa.me/6281234567890" target="_blank">Pesan Sekarang</a>

<!-- Di section kontak -->
<p class="text-gray-600">+62 812-3456-7890</p>
<p class="text-gray-600">Jl. Raya Kuliner No. 123, Jakarta</p>
```

### 3. Menu Items

Edit menu dengan mengubah item yang ada atau menambahkan item baru:

```html
<div class="bg-white rounded-2xl shadow-md overflow-hidden menu-card">
  <div class="overflow-hidden">
    <img src="URL_GAMBAR_MENU" class="w-full h-48 object-cover" alt="Nama Menu">
  </div>
  <div class="p-6 relative">
    <span class="price-tag">Rp Harga</span>
    <h3 class="font-semibold text-lg mb-2">Nama Menu</h3>
    <p class="text-gray-600 text-sm">Deskripsi menu.</p>
    <button class="mt-4 bg-primary hover:bg-secondary text-white px-4 py-2 rounded-full text-sm">Pesan Sekarang</button>
  </div>
</div>
```

### 4. Testimoni Pelanggan

Tambahkan atau edit testimoni pelanggan:

```html
<div class="bg-white p-8 rounded-xl shadow testimonial-card">
  <div class="flex items-center mb-4">
    <div class="w-12 h-12 bg-primary rounded-full flex items-center justify-center text-white font-bold mr-3">Inisial</div>
    <div>
      <h4 class="font-semibold">Nama Pelanggan</h4>
      <div class="flex text-yellow-400">
        <i class="fas fa-star"></i><!-- Tambah bintang sesuai rating -->
      </div>
    </div>
  </div>
  <p class="text-gray-600">"Testimoni pelanggan."</p>
</div>
```

### 5. Google Maps Embed

Ganti embed peta dengan lokasi bisnis Anda:

```html
<iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3966.521260322283!2d106.81956135063955!3d-6.194741395493371!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x2e69f5390917b759%3A0x6e449c18f3bdf51e!2sMonumen%20Nasional!5e0!3m2!1sid!2sid!4v1648012293259!5m2!1sid!2sid" width="100%" height="300" style="border:0; border-radius: 8px;" allowfullscreen="" loading="lazy"></iframe>
```

## 🎯 Customization Guide

### Mengubah Warna Theme

Edit variabel warna di dalam `tailwind.config`:

```javascript
tailwind.config = {
  theme: {
    extend: {
      colors: {
        primary: '#eab308',    // Kuning
        secondary: '#dc2626',  // Merah
        accent: '#16a34a',     // Hijau
        dark: '#1f2937',       // Dark gray
        light: '#f8fafc'       // Light background
      }
    }
  }
}
```

### Menambah Animasi

Beberapa class animasi yang tersedia:
- `animate-bounce-slow` - Bounce effect lambat
- `menu-card` - Hover effect untuk card menu
- `testimonial-card` - Hover effect untuk testimoni

### Gambar dan Media

- Ganti URL gambar dengan gambar produk Anda
- Ukuran optimal untuk gambar menu: 500x400px
- Format gambar: JPG/PNG dengan kompresi optimal

## 📊 SEO Optimization

Website sudah termasuk:

- Meta tags (title, description, keywords)
- Open Graph tags untuk media sosial
- Twitter Card tags
- Schema.org structured data
- Alt tags untuk semua gambar
- Semantic HTML structure

## 📞 Integrasi WhatsApp

Website terintegrasi dengan WhatsApp Business API:

```html
<a href="https://wa.me/6281234567890" target="_blank" class="whatsapp-float">
  <i class="fab fa-whatsapp"></i>
</a>
```

Fitur WhatsApp:
- Tombol mengambang (floating) di sudut kanan bawah
- Tombol pesan di berbagai section
- Pre-filled message untuk pemesanan

## 🚀 Deployment

### Hosting Static

1. Upload file `index.html` ke hosting provider
2. Pastikan semua asset (gambar) terupload
3. Verifikasi semua link berfungsi dengan baik

### Netlify/Vercel

1. Drag and drop folder ke Netlify/Vercel
2. Atau connect repository GitHub
3. Deploy secara otomatis

## 📝 Maintenance

### Update Menu

1. Edit section menu dengan item baru
2. Update harga jika diperlukan
3. Tambahkan gambar menu yang menarik

### Update Testimoni

1. Tambahkan testimoni baru di section testimoni
2. Pastikan rating sesuai dengan ulasan

### Update Informasi

1. Perubahan alamat atau nomor telepon
2. Update jam operasional
3. Perubahan harga atau promo

## 🔍 Analytics dan Tracking

Rekomendasi tools tambahan:

- **Google Analytics** - Track pengunjung website
- **Google Search Console** - Monitor performa SEO
- **Facebook Pixel** - Track conversions dari iklan

## 🤝 Dukungan

Untuk bantuan teknis atau pertanyaan, hubungi:
- Email: contactmhteams.my.id
- Website: [MHTeams](https://mhteams.my.id)

---

**Catatan**: Pastikan untuk menguji semua fungsi website sebelum deploy production, terutama link WhatsApp dan formulir kontak.
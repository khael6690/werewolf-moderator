# 🐺 Werewolf Moderator Dashboard

Dashboard moderator berbasis web untuk memimpin permainan **Werewolf** (Mafia) secara offline. Dirancang khusus untuk dipegang moderator — responsif di mobile, tanpa instalasi, langsung pakai.

🔗 **Live Demo:** [game-xi.vercel.app](https://game-xi.vercel.app)

---

## 📸 Preview

| Setup                        | Distribusi                     | Fase Malam                 | Fase Siang         |
| ---------------------------- | ------------------------------ | -------------------------- | ------------------ |
| ⚙️ Atur jumlah pemain & role | 🃏 Bagikan kartu satu per satu | 🌙 Panduan tiap fase malam | ☀️ Voting eksekusi |

---

## ✨ Fitur

- 🎲 **Generate & acak kartu** otomatis sesuai jumlah pemain
- 🔒 **Distribusi rahasia** — role tersembunyi saat kartu dibagikan, hanya tampil sebentar ke pemain yang bersangkutan
- 🌙 **Panduan fase malam** lengkap dengan skrip narasi untuk moderator (Werewolf → Dokter → Peramal → Hunter)
- 🔮 **Terawangan Peramal** — hasil cek identitas muncul di dashboard tanpa diketahui pemain lain
- 🏹 **Fase Hunter** — otomatis aktif jika Hunter terbunuh, baik malam maupun siang
- 🗳️ **Voting siang** dengan konfirmasi eksekusi
- 📊 **Status bar live** — jumlah pemain hidup, Werewolf, dan mati selalu terupdate
- 🏆 **Deteksi kemenangan otomatis** dengan layar Game Over
- 📱 **Fully responsive** — dioptimalkan untuk HP moderator

---

## 🎭 Role yang Didukung

| Role     | Emoji | Kemampuan                                                              |
| -------- | ----- | ---------------------------------------------------------------------- |
| Warga    | 👤    | Tidak punya kemampuan khusus. Mengandalkan logika saat voting.         |
| Werewolf | 🐺    | Setiap malam memilih satu korban secara diam-diam.                     |
| Peramal  | 🔮    | Setiap malam bisa mengintip identitas satu pemain.                     |
| Dokter   | 💉    | Setiap malam bisa menyelamatkan satu pemain (boleh diri sendiri).      |
| Hunter   | 🏹    | Jika terbunuh (malam/siang), bisa membawa satu pemain mati bersamanya. |

---

## 🚀 Cara Pakai

### Opsi 1 — Langsung Online

Buka link berikut di browser HP moderator:

```
https://game-xi.vercel.app
```

### Opsi 2 — Jalankan Lokal

```bash
git clone https://github.com/[username]/werewolf-moderator.git
cd werewolf-moderator
# Buka index.html di browser
open index.html
```

> Tidak memerlukan server atau instalasi apapun. Cukup buka file HTML.

---

## 🎮 Alur Permainan

```
⚙️  Setup
    └── Atur jumlah pemain & komposisi role

🃏  Distribusi Peran
    └── Moderator ketuk kartu → isi nama → perlihatkan role sebentar → sembunyikan

🌙  Fase Malam (urutan otomatis)
    ├── 🐺 Werewolf memilih korban
    ├── 💉 Dokter menyelamatkan seseorang
    ├── 🔮 Peramal mengintip identitas
    └── 🏹 Hunter membalas (jika terbunuh)

☀️  Fase Siang
    ├── Pengumuman korban semalam
    ├── Diskusi & debat antar pemain
    └── Voting eksekusi

🏆  Game Over
    ├── Warga menang  → Semua Werewolf terbunuh
    └── Werewolf menang → Jumlah WW ≥ Warga
```

---

## 📐 Rekomendasi Komposisi

| Jumlah Pemain | Werewolf | Peramal | Dokter | Hunter |  Warga  |
| :-----------: | :------: | :-----: | :----: | :----: | :-----: |
|      6–7      |    1     |    1    |   0    |   0    |   4–5   |
|     8–10      |    2     |    1    |   1    |   0    |   4–6   |
|     11–13     |    2     |    1    |   1    |   1    |   6–8   |
|     14–16     |    3     |    1    |   1    |   1    |  8–10   |
|      17+      |   3–4    |    1    |   1    |   1    | sisanya |

---

## 🛠️ Tech Stack

- **HTML5** — struktur aplikasi
- **CSS3** — custom dark theme, animasi, responsive layout
- **Vanilla JavaScript** — game logic & state management
- **Bootstrap 5.3** — komponen modal & grid system

> Tidak ada framework, tidak ada backend, tidak ada database. Pure frontend.

---

## 📁 Struktur File

```
werewolf-moderator/
└── index.html      # Seluruh aplikasi dalam satu file
```

---

## 🐛 Bug yang Sudah Diperbaiki

| #   | Deskripsi                                                               | Status   |
| --- | ----------------------------------------------------------------------- | -------- |
| 1   | Input nama tidak muncul setelah menyimpan pemain pertama                | ✅ Fixed |
| 2   | Emoji role tampil di kartu distribusi sehingga bisa ditebak pemain lain | ✅ Fixed |

---

## 📄 Lisensi

MIT License — bebas digunakan dan dimodifikasi.

---

<div align="center">
  Dibuat oleh Khael untuk sesi Werewolf yang lebih seru
</div>

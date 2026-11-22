# Jaxycapie — Fitness Tracker (tampilan iPhone, Liquid Glass)

## Fitur baru
- Tampilan ala aplikasi iOS: tab bar kaca mengambang, bottom sheet, tanpa scroll halaman.
- 3 tema: Terang, Gelap, Liquid Glass (Pengaturan > Tema).
- Alarm: banyak alarm, pilih hari, aktif/nonaktif, tunda 10 menit, uji alarm.
- Streak: hari aktif beruntun (1 latihan selesai ATAU 3 kebiasaan), streak terbaik, lencana 3/7/14/30/60 hari.
- Timer latihan terpandu dengan getar dan bunyi tiap langkah, layar tetap menyala.
- Latar belakang kustom: Pengaturan > Latar belakang > Pilih foto (dari galeri), dengan slider peredup dan blur.
- Animasi halus: layar bergeser ala iOS, indikator tab bar bergerak cair, sheet dan timer lembut.
- Liquid Glass: kilau dan cahaya tepi pada kaca, latar warna yang mengalir pelan (tanpa foto), efek refraksi di Android/Chrome.
- Pelacak air minum dengan target yang bisa diatur, grafik 7 hari.

## Jalankan sebagai aplikasi sungguhan (disarankan, supaya alarm berbunyi saat app ditutup)
Butuh Node.js. Android Studio untuk Android, Xcode (Mac) untuk iPhone.
1. npm install
2. npx cap add android   (dan/atau: npx cap add ios)
3. npm run android       (atau: npm run ios)  -> buka proyek, lalu Run di perangkat.
Alarm memakai plugin LocalNotifications (terjadwal oleh sistem). Di Android 12+,
izinkan "Alarm & pengingat" untuk Jaxycapie di pengaturan sistem bila diminta.

## Jalankan sebagai PWA (tanpa instal toko aplikasi)
Host seluruh isi folder lewat HTTPS (GitHub Pages / Netlify / Cloudflare Pages),
buka di HP, lalu "Add to Home Screen". Di iPhone: Share > Add to Home Screen.
Catatan jujur: PWA tidak bisa menjamin alarm saat aplikasi tertutup.
Mode web hanya membunyikan alarm saat aplikasi terbuka.

## Data
Tersimpan lokal (localStorage). Data lama (move-data) tetap terbaca.

# Petualangan Dungeon — Last Boss

Tiga last boss hanya muncul di Medium, Hard, dan Super Hard. Mode Baby tidak menampilkan bos ini dan tidak memutar animasi horornya.

- Level 25: PErdY ganTeng — HP 30000. Drop kemampuan NPD (101 damage).
- Level 30: mudenSIF1 — HP 120000 (30000 x 4). Drop koin banyak plus Potion, Ether, dan Roti.
- Level 50: GibRal LAstBoss — HP 480000 (30000 x 4 x 4). Drop koin banyak plus Potion, Ether, Roti, dan Potion Kebugaran 2.

## SECRET BOSS: AdMin RoPI (Level 30+)
- Muncul otomatis saat level >= 30 (sekali) atau lewat Kolom Bos.
- HP 100000, ATK 900, regenerasi 50 HP setiap giliran.
- Animasi teks muncul karakter-per-karakter + suara-admin.mp3 saat intro.
- Gambar: Gambar tertanam base64 di HTML (JPG). Nama pakai font khusus merah glitch. 3 fase (HP ×2 tiap fase). Bercak darah muncul saat menyerang.
- Drop: 5 Tiket Emas + 5 Tiket Biasa + Potion x8 + Ether x6 + Roti x8.

HP 30000 dikali 4 tiap tingkatan hanya untuk ketiga bos ini. Bos lain tetap memakai skala lama.
Animasi muncul dan sekarat tampil di layar saat pertarungan dimulai dan saat HP bos di bawah 30%.

Bos Wajah Berganti memutar sahdan.mp3 (berulang) sejak muncul sampai kalah/menang/kembali ke menu.
AdMin RoPI memutar suara-admin.mp3 sekali saat intro (teks istana darah).

Item legendary gacha emas: Busur Ilahi, Tombak Gigi Arya, Sarung Tinju Gibrieal (ATK +400, ability 450); Armor Kulit Arya, Armor Perdy chan, Armor Krocok, Armor Lebah (DEF +300). Kolom Bos tersembunyi, tombol 'Kolom Bos' untuk buka/tutup.

Balance: ability semua senjata legendary 450 tetap (termasuk Pedang PeNebas LauSe); Rem 15 damage; damage Fenrir/Clara/Alder naik lebih lambat.

Update fase & drop:
- Semua boss punya 3 fase (HP bar dibagi 3, ATK naik tiap fase). Gibral 5 fase + regenerasi HP mulai fase 3. Bos Wajah Berganti jadi 3 fase.
- Drop boss: 3 Tiket Emas + 5 Tiket Biasa. Gibral: 5 Tiket Emas + 5 Tiket Biasa.
- Pedang Admin (Mitos, ATK +650, ability 650) peluang 0,6% di Gacha Emas.
- Armor PeNebas LauSe DEF 300 tanpa bonus HP.

Update Super Hard & sistem:
- Super Hard: HP awal Pendekar 95, Pemanah 80, Penyihir 75, Tombak 90.
- Penyihir: skill Heal (MP -25, HP +27), di pertarungan dan di menu utama.
- Album direset saat membuat hero baru dengan nama berbeda (nama sama = album tetap).
- Nama rahasia sekarang "ropi90" ("ropi" tidak lagi memicu kode).


## Pendamping baru: Ropi (dari AdMin RoPI)
- Didapat setelah mengalahkan secret boss **AdMin RoPI**.
- Efek tiap giliran: **+24 Gold** dan **+2 Alkohol**.
- Cerita: admin istana darah yang bertobat setelah dikalahkan, lalu menjadi pendamping.
- Masuk Album (foto admin.jpg / Ropi).

## Update Balance Job & Tampilan HP
- Stat awal & kenaikan level lima Job diseimbangkan agar tiap Job kehilangan HP kurang lebih sama per pertarungan (tidak ada yang terlalu kuat/lemah):
  - Pendekar: ATK 16, naik/level HP+24 ATK+5; skill Tebasan 2.2x ATK (sebelumnya terlalu lemah).
  - Penyihir: HP 95, ATK 15, crit x2.2, HP+14/level; skill 2.0x; tetap punya Heal.
  - Pemanah: HP 105, ATK 15, HP+18/level; tiap panah skill 0.9x.
  - Tombak: ATK 14, crit x2.4, HP+20/level; skill pasti crit 1.2x (sebelumnya terlalu kuat).
  - Petarung: HP 120, ATK 14, dmg [-2,4]; tiap pukulan skill 0.8x.
- HP: panel tombol aksi menempel di bawah layar, tombol lebih besar (min 50px), 2 kolom di HP lebar, area log lebih pendek.

## Update Super Hard, Game Over & Alur Tamat
- Super Hard diperbaiki: musuh 1.5x (dulu 1.7x), stamina 1.3x (dulu 1.6x), gold 0.8x, drop 0.7x; awal 55 stamina dan 30 gold. Critical dibatasi x1.5 di Level <10, x1.8 di Level 10-19, normal mulai Level 20.
- Layar game over / tamat: efek darah (bercak & aura merah AdMin RoPI) dihapus.
- Layar game over menampilkan ringkasan stat dan semua ability (skill job, Heal, kemampuan master, ability pedang/legendary, NPD).
- Alur tamat diselaraskan: tamat = Naga Raja + 3 boss rahasia (ending biasa). Di Super Hard, Botak Kopral hanya wajib jika kamu punya Elf Clara (ending romantis Clara). Tanpa Clara, Super Hard tamat dengan ending biasa. Boss level (Perdy, Muden, Gibral) tidak punya ending sendiri.

## Perbaikan Bug: Ropi di Toko Budak
- Ropi tidak lagi muncul/bisa dibeli di Toko Budak. Ropi HANYA didapat dari drop setelah mengalahkan secret boss AdMin RoPI.


## Update Balance v4 (koin, potion, musuh krocok, alkohol, Heal, Stunt, Master)
- **Drop koin -10%**: semua koin dari monster & bos x0,9 (konstanta `FAKTOR_KOIN`). Bos: Dark Pulse 3600, Ipulattor 4500, Muden 5400, Gibral 10800, Spongebob 270.
- **Potion**: sekarang memulihkan **15% HP maksimal** (bukan +50 flat). Label toko & battle ikut berubah.
- **Musuh krocok/lemah di dungeon**: tiap player naik 4 level (Lv 5, 9, 13, ...) HP musuh **x2** dan damage musuh **+1,5%** (kumulatif per tingkat). Konstanta `KROCO_*`. Boss tidak terpengaruh.
- **Alkohol**: efek **2 aksi**; selama itu serangan musuh **tidak memberi damage** (aksi tetap gratis). Setelah efek habis, **stamina jadi 0** (penalti HP -20% diganti ini). MP tetap dikembalikan.
- **Penyihir Heal**: pulihkan **15% HP maks**, biaya **MP 15 + stamina 6** (di battle & menu utama).
- **Petarung - Stunt**: tombol aksi baru, **-10 stamina**, musuh **tidak bisa menyerang 2 giliran**. Tidak bisa ditumpuk selagi aktif.
- **Kemampuan Master di tombol aksi**: Tebasan Maut (Pendekar) dan skill master job lain kini muncul sebagai tombol di battle setelah terbuka lewat latihan di Master Job (3 latihan per kemampuan). Sebelumnya skill ini sudah terbuka tapi belum punya tombol.


## Update v5 — Potion, Gibral, Ipulattor, Istirahat
- Potion memulihkan **25% HP maksimal** (bukan 15%).
- Istirahat biaya **14 gold** di semua kesulitan.
- **GibRal LAstBoss**: foto diganti (portrait baru), suara `boss-gibral.mp3` (~10 detik) saat muncul, teks intro diketik selama ~10 detik, font & animasi merah glitch menyeramkan.
- **The Man Ipulattor**: HP 10000, ATK 200; Kroco Kartu HP 9000 ATK 100; HP selalu tersembunyi; animasi kartu remi beterbangan (gaya Joker) saat muncul/serang.

## Update gacha
- Menu gacha tetap dua: Gacha Biasa dan Gacha Emas. Peluang tidak diubah.
- Animasi gacha sering menampilkan Rem.

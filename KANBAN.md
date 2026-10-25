# Kanban — Aplikasi Presensi Praktikum

**Sprint 2 · Fokus: US8 — Pencarian nama mahasiswa**  
**Sprint Goal:** Menambahkan pencarian nama tanpa merusak fitur Sprint 1.

Status berikut mengikuti simulasi pada [laporan](LAPORAN_US8.md), bukan pelacakan pekerjaan secara langsung.

Papan Kanban memperlihatkan posisi setiap User Story selama Sprint 2. Kolom menunjukkan status pekerjaan, sedangkan kartu menunjukkan User Story yang diproses.
**Arti kolom:**
- **Backlog:** belum dikerjakan pada Sprint 2.
- **Dikerjakan:** sedang diimplementasikan.
- **Review/Uji:** implementasi selesai dan sedang diperiksa melalui pengujian.
- **Selesai:** fitur telah diimplementasikan dan pengujiannya lulus.

**Batas WIP (*Work in Progress*):** kolom Dikerjakan maksimal 2 kartu dan kolom Review/Uji maksimal 1 kartu.

### 4.1 Papan Awal Sprint 2 — Perencanaan

US8 dipilih sebagai pekerjaan Sprint 2. US1–US7 merupakan fitur yang sudah selesai dari Sprint 1, sedangkan US9 dan US10 belum dipilih untuk dikerjakan.

| BACKLOG — Belum dikerjakan                 | DIKERJAKAN — Maks. 2 kartu                     | REVIEW/UJI — Maks. 1 kartu | SELESAI                            |
|--------------------------------------------|------------------------------------------------|----------------------------|------------------------------------|
| **US9** — Presensi dibedakan per pertemuan | **US8** — Pencarian mahasiswa berdasarkan nama |        — Belum ada —       | **US1** — Input identitas          |
| **US10** — Mengedit status presensi        |                                                |                            | **US2** — Memilih status presensi  |
|                                            |                                                |                            | **US3** — Validasi NIM             |
|                                            |                                                |                            | **US4** — Mencegah NIM duplikat    |
|                                            |                                                |                            | **US5** — Melihat daftar presensi  |
|                                            |                                                |                            | **US6** — Melihat rekap presensi   |
|                                            |                                                |                            | **US7** — Menyimpan data ke CSV    |

### 4.2 Papan Pertengahan Sprint 2 — Menunggu Pengujian

Setelah fungsi pencarian dan integrasi menu selesai, kartu US8 dipindahkan dari kolom Dikerjakan ke Review/Uji. Fitur belum dipindahkan ke Selesai sampai pengujian dilakukan.

| BACKLOG — Belum dikerjakan          | DIKERJAKAN — Maks. 2 kartu | REVIEW/UJI — Maks. 1 kartu                                             | SELESAI                      |
|-------------------------------------|----------------------------|------------------------------------------------------------------------|------------------------------|
| **US9** — Presensi per pertemuan    |         — Tidak ada —      | **US8** — Pencarian nama; periksa kriteria penerimaan dan jalankan tes | **US1–US7** — Fitur Sprint 1 |
| **US10** — Mengedit status presensi |                            |                                                                        |                              |

**Daftar pemeriksaan pada tahap Review/Uji:**

| Pemeriksaan                                  | Status yang dituju |
|----------------------------------------------|--------------------|
| Pencarian sebagian nama                      | Lulus              |
| Pencarian tidak membedakan huruf besar/kecil | Lulus              |
| Kata kunci tidak ditemukan                   | Lulus              |
| Kata kunci kosong atau hanya spasi           | Lulus              |
| Berkas CSV belum tersedia                    | Lulus              |
| Seluruh tes lama tetap lulus                 | Lulus              |

### 4.3 Papan Akhir Sprint 2 — Pengujian Lulus

Setelah seluruh pengujian selesai dan lulus, US8 dipindahkan ke kolom Selesai. US9 dan US10 tetap di Backlog karena belum dikerjakan dalam Sprint 2.

| BACKLOG — Sprint berikutnya         | DIKERJAKAN — Maks. 2 kartu | REVIEW/UJI — Maks. 1 kartu | SELESAI                                        |
|-------------------------------------|----------------------------|----------------------------|------------------------------------------------|
| **US9** — Presensi per pertemuan    |        — Tidak ada —       |        — Tidak ada —       | **US1** — Input identitas                      |
| **US10** — Mengedit status presensi |                            |                            | **US2** — Memilih status presensi              |
|                                     |                            |                            | **US3** — Validasi NIM                         |
|                                     |                            |                            | **US4** — Mencegah NIM duplikat                |
|                                     |                            |                            | **US5** — Melihat daftar presensi              |
|                                     |                            |                            | **US6** — Melihat rekap presensi               |
|                                     |                            |                            | **US7** — Menyimpan data ke CSV                |
|                                     |                            |                            | **US8** — Pencarian mahasiswa berdasarkan nama |

## Pergerakan US8 selama Sprint 2

| Tahap | Backlog | Dikerjakan | Review/Uji | Selesai |
|---|---|---|---|---|
| Awal sprint | US9, US10 | **US8** | — | US1–US7 |
| Pertengahan sprint | US9, US10 | — | **US8** | US1–US7 |
| Akhir sprint | US9, US10 | — | — | US1–US8 |

**Penerapan WIP limit:** saat US8 berada di kolom Review/Uji, tim tidak menarik pekerjaan baru ke kolom tersebut karena batasnya satu kartu. Pengujian US8 diselesaikan terlebih dahulu. US9 dan US10 tetap berada di Backlog untuk dipertimbangkan pada Sprint berikutnya.

**Catatan:** papan ini menggambarkan status awal, pertengahan, dan akhir Sprint sebagaimana dicatat dalam laporan. Jika dosen meminta bukti penggunaan alat Kanban digital, lampirkan tangkapan layar papan yang benar-benar dibuat atau digunakan oleh kelompok.
---

## Detail kartu US8

> Sebagai dosen, saya ingin mencari nama mahasiswa agar dapat menemukan data presensi dengan cepat tanpa membaca seluruh daftar.

**Prioritas:** Tinggi · **Estimasi:** 2 story point · **Sprint:** 2

### Kriteria penerimaan

- Pencarian tersedia melalui menu 4, **Cari nama**.
- Mendukung pencarian sebagian nama.
- Tidak membedakan huruf besar dan kecil.
- Kata kunci kosong atau hanya spasi menampilkan seluruh data.
- Hasil yang tidak cocok menampilkan pesan data tidak ditemukan.
- Berkas CSV yang belum ada menghasilkan daftar kosong tanpa error.
- Urutan hasil mengikuti urutan data dalam berkas.

### Syarat pindah ke Selesai

- Seluruh kriteria penerimaan terpenuhi.
- Tes pencarian dan tes fitur lama lulus.
- Fitur berhasil didemonstrasikan melalui terminal.
- Laporan dan video demonstrasi diunggah.

**Catatan:** Status US8 mengikuti laporan. Tautan unggahan laporan dan video masih perlu diisi pada laporan untuk melengkapi bukti Definition of Done.

## Aturan papan

1. Alur kartu: **Backlog → Dikerjakan → Review/Uji → Selesai**.
2. Maksimal dua kartu berada di Dikerjakan dan satu kartu di Review/Uji.
3. Selesaikan pengujian US8 sebelum menarik pekerjaan berikutnya, sesuai kebijakan tim dalam laporan.
4. Kartu yang gagal diuji dikembalikan ke Dikerjakan dengan catatan perbaikan.
5. US9 dan US10 tetap di Backlog sampai dipilih dalam perencanaan sprint berikutnya.

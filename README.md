# Simulasi Sistem Kontrol Kecepatan Kereta Monorail Menggunakan PID Controller

Repositori ini berisi simulasi sistem kendali kecepatan kereta monorail menggunakan PID Controller berbasis MATLAB/Simulink. Proyek ini merupakan Laporan Tugas Akhir Praktikum Teknik Kendali dan Otomasi, Departemen Teknik Komputer, Universitas Diponegoro (2026).

## 👥 Tim Penyusun
- Enrico Gathan Agung (21120123140127)
- Saiful Mustofa (21120123130049)
- Gibson Lasoni Gea (21120123120028)
- Shata' Hibrizi Al Fa'iq (21120123130066)
- Alif Arlendi Putra Priyanto (21120123140042)
- Ian Widi Antaressa (21120123140137)

## 📖 Deskripsi Proyek
Monorail merupakan sistem transportasi berbasis rel tunggal yang membutuhkan kestabilan kecepatan agar pergerakan kereta aman dan nyaman. Proyek ini memodelkan sistem penggerak monorail sebagai motor DC orde satu dan mengendalikan kecepatannya menuju *setpoint* 1 m/s menggunakan konfigurasi kontrol *closed-loop* dengan PID Controller.

## ⚙️ Parameter Sistem
* **Plant Motor DC:** $G(s) = \frac{1}{0.5s+1}$
* **Setpoint Kecepatan:** 1 m/s
* **PID Controller:**
    * Proportional ($K_p$): 15
    * Integral ($K_i$): 2
    * Derivative ($K_d$): 10

## 🚀 Cara Menjalankan Simulasi
Simulink *model* dibangun secara otomatis menggunakan *script* MATLAB.
1. Buka aplikasi MATLAB.
2. Buat *script* baru dan salin kode dari bagian `3.6. Program MATLAB` pada laporan.
3. Jalankan *script* (Run).
4. MATLAB akan secara otomatis membuat, merangkai, dan menyimpan file model Simulink bernama `PID_Monorail_Control.slx`.
5. Buka blok `Scope` pada model Simulink yang telah dibuat untuk melihat hasil simulasi.

## 📊 Hasil dan Analisis
Berdasarkan perancangan sistem dan perhitungan matematis, diperoleh:
* **Fungsi Alih Sistem Closed-Loop:** $T(s) = \frac{10s^2 + 15s + 2}{10.5s^2 + 16s + 2}$
* **Pole Sistem:** $s_1 = -1.386$ dan $s_2 = -0.137$. Karena seluruh akar bernilai negatif dan berada di sebelah kiri bidang-s, maka sistem dinyatakan **stabil**.
* **Kinerja Respon:** Sistem dapat mencapai *steady-state* dengan *error* akhir yang mendekati nol, *overshoot* tidak signifikan, dan *settling time* pada batas toleransi $\pm 2\%$ berada di sekitar 9.22 detik. Kombinasi parameter PID terbukti efektif mengatur kecepatan kereta monorail mengikuti nilai referensi.

## 📚 Referensi Pembelajaran Terkait
* Ogata, K. (2010). *Modern Control Engineering* (5th ed.). Prentice Hall.
* Nise, N. S. (2015). *Control Systems Engineering* (7th ed.). John Wiley & Sons.

# Learning-CPP
History of C++ basic programming learning, mixed from many online platform (ex. TLX, Coddy, etc soon)

============ REKURSI ============
(Source TLX)
Fungsi rekursi merupakan fungsi dimana kita tidak melakukan perulangan (loop) dalam programnya.
Biasanya digunakan dalam perhitungan matematika seperti Faktorial.

 int faktorial(int n) {
    if (n == 1) {
         return 1;
     } else {
         return faktorial(n - 1) * n;
     }
 }

Cara jalannya kode secara berurutan :
1. Cek input n, ambil contoh n = 4
2. Cek if statement, karna n != 1 maka kita skip dan lanjut ke blok kode else
3. Kita "return faktorial(4-1) * n;" maka menjadi "return faktorial(3) * 4". Nahhh, tapi kita belum tau nilai dari faktorial(3) maka kita perlu cari tau dulu nilainya
4. Kita "return faktorial(3-1) * n;" maka menjadi "return faktorial(2) * 3". Nahhh, tapi kita belum tau nilai dari faktorial(2) maka kita perlu cari tau dulu nilainya
5. Kita "return faktorial(2-1) * n;" maka menjadi "return faktorial(1) * 2". Kita cek bahwa nilai dari faktorial(1), karena sama dengan if statement maka kita return nilai dari faktorial(1) = 1 dan hasilnya dari faktorial(2) adalah return 1 * 2 = 2. faktorial(2) = 2
6. Bentuk dari "faktorial(2-1) * 2" didapat jika kita memanggil fungsi "int faktorial(2)" maka disini kita update nilai dari faktorial(2) yaitu faktorial(1) * 2 dan hasilnya adalah 2.
7. Bentuk dari "faktorial(3-1) * 3" didapat jika kita memanggil fungsi "int faktorial(3)" maka disini kita update nilai dari faktorial(3) yaitu faktorial(2) * 3 dan hasilnya adalah 6.
8. Bentuk dari "faktorial(4-1) * 4" didapat jika kita memanggil fungsi "int faktorial(4)" maka disini kita update nilai dari faktorial(4) yaitu faktorial(3) * 4 dan hasilnya adalah 24.
9. Maka nilai dari 4! = 24, dan ini benar secara perhitungan manual juga.

Secara umum, sebuah fungsi rekursif terdiri atas dua bagian:
- Kasus dasar (base case): nilai fungsi bisa dihitung langsung tanpa rekursi.
  > Untuk fungsi faktorial di atas, kasus ini adalah ketika n == 1 maka kita langsung return 1;.
- Langkah rekursif (recursive step): nilai fungsi dihitung dengan rekursi.
  > Untuk fungsi faktorial di atas, kasus ini adalah kasus selain n == 1 (yakni n lebih besar dari 1), maka hasilnya adalah faktorial(n - 1) * n.
  > (Perhatikan bahwa fungsi ini mengasumsikan n adalah bilangan positif.)
Perhatikan bahwa kasus dasar harus ada. Tanpanya, fungsi rekursif akan memanggil dirinya sendiri tanpa henti!

NOTES!
  Cara kerja sederhana dari rekursi adalah dengan:
  1) Mengecek fungsi yang dipanggil dengan nilai yang turun (dari n hingga 1)
  2) Jika sudah sampai 1, maka nilainya akan diupdate naik (dari 1 hingga n)

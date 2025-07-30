# collab-roblok

ini adalah proyek sederhana untuk belajar kolaborasi menggunakan Git & Android Studio

##👥 Tim  
-Amelia Nur Auni :inisialisasi & merge pr

-Erikza Assyifia Ahmad : fitur TextView

-Jovita Acid Rahayu : fitur Button

 ##📱Fitur
 
 -Menampilkan TextView

-Menampilkan button yang dapat diklik

<img src="https://github.com/user-attachments/assets/ba4c6d03-191d-41ac-9548-88e82cba8124" alt="Gambar WhatsApp" width="300"/>

##🔧Teknologi

-Kotlin

Kotlin itu adalah bahasa pemrograman yang sekarang banyak dipakai buat bikin aplikasi Android. Kotlin dikembangkan oleh JetBrains dan didukung langsung oleh Google, jadi sudah jadi standar baru di dunia Android. Dibandingkan Java, Kotlin lebih singkat penulisannya, lebih mudah dibaca, dan lebih aman.

-Android Studio

Android Studio adalah aplikasi utama yang dipakai buat ngoding Android. Di sini kamu bisa nulis kode, desain tampilan aplikasi, ngejalanin emulator, dan juga nge-debug kalau ada error. 

-Git + GitHub

Git dan GitHub penting banget buat ngatur versi kode. Git itu kayak mesin pencatat semua perubahan yang kamu lakukan di kode — jadi kalau ada yang salah, kamu bisa mundur ke versi sebelumnya.


##Penjelasan code penting  

<img width="304" height="145" alt="Cuplikan layar 2025-07-30 130522" src="https://github.com/user-attachments/assets/8ea155c5-7d5e-4266-98ed-e2c69dd7ecb6" />

* android.os.Bundle
 =>Ini dipakai buat nyimpen data sementara saat aplikasi dibuka. Biasanya dipakai di onCreate() biar data tetap aman waktu aplikasi berubah-ubah posisi.

* android.widget.Button
=> Supaya kamu bisa pakai tombol (Button) di aplikasi.

* android.widget.EditText
=> Ini buat bikin kolom input, misalnya untuk ngetik nama, email, atau biodata.

* android.widget.TextView
=> Dipakai buat nampilin tulisan ke layar. Contohnya teks “Form Biodata Siswa” di aplikasi kamu.

* androidx.activity.enableEdgeToEdge
=> Fungsinya buat bikin tampilan aplikasi bisa penuh sampai ke ujung layar, biar lebih modern dan kekinian.

* androidx.appcompat.app.AppCompatActivity
=> Ini adalah activity utama yang sering banget dipakai. Fungsinya bantu supaya aplikasi kamu tetap jalan di Android versi lama maupun baru.

* androidx.core.view.ViewCompat dan WindowInsetsCompat
=> Dua ini bantu kamu ngatur tampilan biar bisa menyesuaikan notch, status bar, atau bagian atas/bawah layar yang kadang kepotong. Jadi aplikasi kelihatan lebih rapi di semua HP.

<img width="454" height="136" alt="Cuplikan layar 2025-07-30 131711" src="https://github.com/user-attachments/assets/63b88247-be75-4ae6-bece-2d3a3581486e" />

* private: artinya variabel ini hanya bisa diakses dari dalam class itu sendiri (nggak bisa dipakai dari luar).

* lateinit: artinya variabel ini akan diinisialisasi nanti, bukan langsung saat dibuat. Ini cuma bisa dipakai untuk variabel yang bukan null, dan tipenya harus bisa diubah (bukan val).

* var: artinya variabel ini bisa berubah nilainya.

<img width="221" height="40" alt="Cuplikan layar 2025-07-30 131954" src="https://github.com/user-attachments/assets/8328c4bf-cbe9-40cc-9d72-548d03fcb831" />

override fun onCreate adalah fungsi yang dijalankan saat aplikasi pertama kali dibuka. Di sini, kamu menyiapkan tampilan dan logika awal, seperti menghubungkan tombol dan input. Kata override artinya kamu menimpa fungsi bawaan Android agar sesuai dengan kebutuhan aplikasi kamu.

<img width="419" height="32" alt="Cuplikan layar 2025-07-30 132738" src="https://github.com/user-attachments/assets/e6506a4b-4ee1-4d4e-adfc-8ad2c06cd24f" />

setContentView(R.layout.activity_main) berfungsi untuk menampilkan file XML bernama activity_main.xml sebagai tampilan utama aplikasi saat activity dijalankan. Jadi, semua tombol, input teks, dan elemen UI yang kamu desain di file activity_main.xml akan muncul di layar.

<img width="430" height="114" alt="Cuplikan layar 2025-07-30 133140" src="https://github.com/user-attachments/assets/e421d974-adf8-4a17-a8a3-8397a619672d" />

* findViewById(R.id.etNama) -> mencari input teks bernama etNama di layout dan menghubungkannya ke variabel inputName.

* findViewById(R.id.etKelas) -> menghubungkan kolom input kelas ke variabel inputKelas.

* findViewById(R.id.btnTampilkan) -> menghubungkan tombol ke variabel btnSubmit.

* findViewById(R.id.tvHasil) -> menghubungkan TextView tempat hasil akan ditampilkan ke variabel txtResult.

<img width="510" height="147" alt="Cuplikan layar 2025-07-30 133436" src="https://github.com/user-attachments/assets/d8366b83-8cd8-43c1-88aa-7daf82bbf871" />

* btnSubmit.setOnClickListener { ... } -> Saat tombol btnSubmit ditekan (diklik oleh pengguna), semua kode di dalam kurung kurawal {} akan dijalankan
  
* val nama = inputName.text.toString().trim() -> inputName adalah kolom tempat pengguna mengetik nama , text mengambil isi teks dari kolom itu , toString() mengubah isi tersebut ke bentuk String (teks) , trim() menghapus spasi kosong di awal dan akhir.
*  val kelas = inputKelas.text.toString().trim() -> Sama seperti sebelumnya, tapi ini untuk variabel kelas.
*  val hasil = "Nama: $nama\nKelas: $kelas" -> Baris ini menyusun teks yang akan ditampilkan ke pengguna.
$nama dan $kelas mengambil nilai dari variabel yang sudah dibuat tadi.\n berarti baris baru (enter).
* txtResult.text = hasil -> untuk menampilkan hasil yang tadi dibuat ditampilkan ke TextView dengan ID txtResult.

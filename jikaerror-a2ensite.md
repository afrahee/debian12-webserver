Apabila mengalami error ini <code>bash: a2ensite: command not found</code> bisa ikuti langkah-langkah di bawah ini:

📌 Masalahnya sekarang adalah direktori /usr/sbin belum masuk ke $PATH dalam sesi terminal Anda (meskipun Anda sudah root).

✅ Solusi: Tambahkan /usr/sbin ke PATH
Jalankan perintah ini agar a2ensite bisa dikenali:

<pre><code>export PATH=$PATH:/usr/sbin</code></pre>

Setelah itu, jalankan:
<pre><code>a2ensite wordpress</code></pre>
  
Lalu reload Apache:
<pre><code>systemctl reload apache2</code></pre>

🔄 (Opsional) Agar permanen setiap login:
Tambahkan ke file konfigurasi shell root (.bashrc atau .profile):
<pre><code>echo 'export PATH=$PATH:/usr/sbin' >> ~/.bashrc </code></pre>
<pre><code>source ~/.bashrc </code></pre>

🚀 Selanjutnya
Jika a2ensite wordpress berhasil, lanjut ke langkah akhir WordPress:

<pre><code>Akses di browser: http://<ip-vm-anda>/wordpress</code></pre>

Silahkan lanjutkan proses instalasinya. Lihat file 

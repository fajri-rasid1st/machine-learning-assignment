# _Clustering_

_**Clustering**_ adalah sebuah proses untuk mengelompokkan data ke dalam beberapa _cluster_ atau kelompok sehingga data dalam satu _cluster_ memiliki tingkat kemiripan yang maksimum dan data antar _cluster_ memiliki kemiripan yang minimum (Tan, 2006). Objek di dalam _cluster_ memiliki kasamaan karakteristik antar satu sama lain dan berbeda dengan _cluster_ yang lain. Partisi dilakukan dengan suatu algoritma _clustering_. _Clustering_ sangat berguna karena mampu menemukan _group_ atau kelompok yang tidak dikenal dalam data. _Clustering_ banyak digunakan dalam berbagai aplikasi seperti misalnya pada _business inteligence_, pengenalan pola citra, _web search_, bidang ilmu biologi, dan untuk keamanan (_security_).

Beberapa metode dalam melakukan _clustering_ adalah sebagai berikut.

## _K-Means_

_K-Means_ merupakan salah satu algoritma klastering dengan metode partisi (_partitioning method_) yang berbasis titik pusat (_centroid_) selain algoritma _k-Medoids_ yang berbasis obyek. Berikut adalah algoritma _K-Means._

>- Tentukan berapa banyak_ cluster k_ dari _dataset_ yang akan dibagi.
>- Tetapkan secara acak data _k_ menjadi pusat awal lokasi klaster.
>- Untuk masing-masing data, temukan pusat_ cluster _terdekat. Dengan demikian berarti masing-masing pusat_ cluster _memiliki sebuah subset dari _dataset_, sehingga mewakili bagian dari _dataset_. Oleh karena itu, telah terbentuk_ cluster k: C1, C2, C3, …, Ck._
>- Untuk masing-masing_ cluster k_, temukan pusat luasan klaster, dan perbarui lokasi dari masing-masing  pusat_ cluster _ke nilai baru dari  pusat luasan.
>- Ulangi langkah ketiga dan kelima hingga data pada tiap_ cluster _menjadi terpusat atau selesai.

## _K-Medoids_

_K-Medoids_ adalah metode _cluster_ non hirarki yang merupakan varian dari metode _K-Means_. _K-Medoids_ hadir untuk mengatasi kelemahan _K-Means_ yang sensitif terhadap _outlier_ karena suatu objek dengan suatu nilai yang besar mungkin secara substansial menyimpang dari distribusi data (Jiawei &amp; Kamber, 2006). Hal ini didasarkan pada penggunaan _medoids_ bukan dari pengamatan mean yang dimiliki oleh setiap _cluster_, dengan tujuan mengurangi sensitivitas dari partisi sehubungan dengan nilai ekstrim yang ada dalam _dataset_ (Vercellis, 2009). Langkah-langkah pada metode _K-Medoids_ adalah:

>- Tentukan _k _(jumlah _cluster_) yang diinginkan
>- Pilih secara acak _medoid_ awal sebanyak _k _dari _n_ data
>- Hitung jarak masing-masing objek ke _medoid_ sementara, kemudian tandai jarak terdekat objek ke _medoid_ dan hitung totalnya.
>- Lakukan iterasi _medoid._
>- Hitung total simpangan (_S_). Jika _a_ adalah jumlah jarak terdekat antara objek ke _medoid_ awal, dan b adalah jumlah jarak terdekat antara objek ke _medoid_ baru, maka total simpangan adalah _S = b - a_, Jika _S < 0_, maka tukar objek dengan data untuk membentuk sekumpulan _k_ baru sebagai _medoid_.
>- Ulangi langkah 3 sampai 5 dan hentikan jika sudah tidak terjadi perubahan anggota _medoid._

## _Hierarchical Clustering_

Pada _hierarchical clustering_ data dikelompokkan melalui suatu bagan yang berupa hirarki, dimana terdapat penggabungan dua grup yang terdekat disetiap iterasinya ataupun pembagian dari seluruh set data kedalam _cluster_. Langkah-langkah melakukan _Hierarchical clustering_:

>- Identifikasi item dengan jarak terdekat.
>- Gabungkan item itu kedalam satu _cluster._
>- Hitung jarak antar _cluster_.
>- Ulangi dari awal sampai semua terhubung.

## _Density-Based Spatial Clustering of Application with Noise (DBSCAN)_

_Density-Based Spatial Clustering of Application with Noise (DBSCAN)_ merupakan sebuah metode _clustering_ yang membangun area berdasarkan kepadatan yang terkoneksi (_density-connected_). Setiap objek dari sebuah radius area (_cluster_) harus mengandung setidaknya sejumlah minimum data. Semua objek yang tidak termasuk di dalam _cluster_ dianggap sebagai _noise_. Komputasi dari _DBSCAN_ adalah sebagai berikut.

>- Inisialisasi parameter _minpts, eps._
>- Tentukan titik awal atau _p_ secara acak.
>- Ulangi langkah 3 sampai 5 hingga semua titik diproses.
>- Hitung _eps_ atau semua jarak titik yang _density reachable_ terhadap _p_.
>- Jika titik yang memenuhi _eps_ lebih dari _minpts_ maka titik _p_ adalah _core point_ dan _cluster_ terbentuk.
>- Jika _p_ adalah _border point_ dan tidak ada titik yang _density reachable_ terhadap _p_, maka proses dilanjutkan ke titik yang lain.
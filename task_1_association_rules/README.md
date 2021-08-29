# _Association Rules Mining_

_**Association Rules Mining**_ adalah teknik _data mining_ yang bertujuan untuk menemukan aturan asosiatif antara suatu kombinasi item pada data.Contoh aturan asosiatif dari analisa pembelian di suatu supermarket adalah dapat diketahui seberapa besar kemungkinan seorang pelanggan membeli roti bersamaan dengan susu. Secara umum, _association rules_ mempunyai bentuk, dimana dan tersebut adalah himpunan item. Jika setiap item dalam terdapat dalam transaksi, maka setiap item dalam juga terdapat dalam transaksi.

Terdapat tiga parameter penting yang sering digunakan dalam menentukan aturan _(rules)_ yang menarik,

_**1. Support**_

_**Support**_ dari suatu _association rules_ adalah persentasi kombinasi item tersebut dalam _database_, dimana jika terdapat item A dan item B maka _support_ adalah proporsi dari transaksi dalam _database_ yang mengandung A dan B.

_**2. Confidence**_

_**Confidence**_ dari _association rules_ adalah ukuran ketepatan suatu _rule_, yaitu persentasi transaksi dalam _database_ yang mengandung A dan mengandung B. Dengan adanya _confidence_ kita dapat mengukur kuatnya hubungan antar item dalam _association rules_.

_**3. Lift Ratio**_

_**Lift Ratio**_ adalah suatu ukuran untuk mengetahui kekuatan aturan asosisasi yang telah terbentuk. Nilai _lift ratio_ biasanya digunakan sebagai penentu apakah aturan asosiasi valid atau tidak valid.

# _Apriori Algorithm_

_Apriori Algorithm_ menggunakan frekuensi _itemsets_ untuk menghasilkan aturan asosiasi. Algoritma ini banyak digunakan untuk bekerja pada _database_ yang berisi transaksi. Algoritma _Apriori_ memiliki langkah-langkah sebagai berikut.

> -   Menentukan minimum _support_.
> -   Iterasi 1, hitung setiap item dari _support_ (transaksi yang memuat seluruh item) dengan melakukan _scan database_ untuk _1-itemset_, setelah _1-itemset_ didapatkan, dari _1-itemset_ tersebut apakah berada di atas minimum _support_, apabila telah memenuhi minimum _support_, _1-itemset_ tersebut akan menjadi pola frekuensi tinggi.
> -   Iterasi 2, untuk mendapatkan _2-itemset_, perlu dilakukan kombinasi dari _k-itemset_ sebelumnya, kemudian _scan database_ untuk menghitung setiap item yang memuat _support_. _Itemset_ yang memenuhi minimum _support_ akan dipilih sebagai pola frekuensi tinggi dari kandidat.
> -   Tetapkan nilai _k-itemset_ dari _support_ yang telah memenuhi minimum _support_ dari _k-itemset_.
> -   Lakukan proses untuk iterasi selanjutnya hingga tidak ada lagi _k-itemset_ yang memenuhi minimum _support_.

# _Frequent Pattern Growth Algorithm (FP-Growth)_

Algoritma _FP-Growth_ merupakan perbaikan dari Algoritma _Apriori_. Berbeda dengan algoritma _Apriori_ dimana kita menghasilkan kandidat _frequent-itemset_ di setiap iterasi, _FP-Growth_ bekerja dengan menggunakan _FP-Tree_. Adapun langkah-langkah dalam algoritma _FP-Growth_ adalah sebagai berikut.

> -   Deduksi item yang sering dipesan. Untuk item dengan frekuensi yang sama, urutannya diberikan menurut urutan abjad.
> -   Bangun _FP-Tree_ berdasarkan transaksi yang tersedia.
> -   Dari _FP-Tree_ yang ada, buat _FP-conditional tree_ untuk setiap item atau _itemset_.
> -   Tentukan pola _frequent pattern._

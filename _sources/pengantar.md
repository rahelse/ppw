# Pengantar 
## Pengantar Web Mining
Web mining merupakan teknik data mining dan machine learning untuk menggali informasi dari data web (konten, struktur, dan pengunaan), dengan membayangkan kamu suka melakukan pencarian dengan google  
Dengan tujuan utamanya adalah menemukan pola, pengetahuan, atau insight dari data web.

## Web Crawling
Nah sebelum bisa "menggali" dari data web, kita membutuhkan cara buat mengambil datanya. Web Crawling adalah proses otomatis untuk menjelajahi halaman web satu per satu menggunakan robot kecil (disebut crawler/spider/bot). Crawler mulai dari satu halaman, lalu mengikuti link-link yang ada didalamnya sampai terkumpul banyak data.
yang biasa menggunakan :
1. Scrapy (Python) framework crawling
2. BeautifulSoup (Python) ambil teks dari HTML
3. Selenium buat crawling web yang butuh interaksi (dengan contoh harus klik tombol dulu)

## Web Data Processing
Data web yang kita ambil biasanya "kotor" banyak tag HTML, script, iklan, dan simbol aneh. Maka, processing itu digunakan untuk membersihkan dan merapikan data sebelum dipakai.
tahap tahap pada umumnya :
1. Parsing HTML (mengambil konten inti yaitu judul, isi artikel)
2. Cleaning teks (menghapus angka, tanda baca, simbol)
3. Stopword removal (hapus kata umum seperti 'dan', 'atau')
4. Stemming (mengubah kata ke bentuk dasar seperti 'berlari' ke 'lari')
5. representasi data (yaitu mengubah teks jadi angka TF-IDF)

## Pembelajaran Terawasi (Supervised Learning)
1. dapat dicontohkan dengan kita memberikan data + label ~ model belajar berhubungan keduanya
2. setelah itu, kita memiliki data baru (tanpa label)model bisa tebak jawabannya
menggunakan algoritma umum yaitu Decesion Tree, Naive Bayes, Logistic Regression, SVM, Neural Networks

## Pembelajaran Tak Terawasi (Unsupervised Learning)
kebalikan dari belajar tanpa label, jadi model hanya memberikan data mentah lalu mencari pola sendiri
menggunakan algoritma umum K-Means, Hierarchical Clustering, DBSCAN, PCA, LDA

## Web Content Mining
 melihat isi pencarian (judul, deskripsi jadi lebih fokus kepada isi web)
 menggunakan teknik :
 1. Text Classification 
 2. Sentiment Analysis
 3. Named Entity Recognition
 4. Keyword Extraction

 ## Web Usage Mining
 melihat kebiasaan kamu melakukan pencarian (jam berapa, pencarian apa, jadi lebih fokus kepada perilaku perilaku pengguna)
 Menggunakan Teknik :
 1. Google Analytics, Matomo
 2. Apache log parser, Hadoop/spark untuk data besar

 ## Web Structure Mining
melihat hubungan antar pencarian (pencarian A mirip dengan pencarian B, jadi lebih fokus pada hubungan antar situs) 
Menggunaka  teknik :
1. NetworkX (Python) ~ analisis graph
2. Gephi 
3. neo4j

## Deployment System
Kalau semua sudah jadi (crawling ~ preprocessing ~ modeling) langkah terakhir adalah deplot sistem supaya dapat digunakan orang lain
dengan cara :
1. Buat API (bisa menggunakan Flask,FastAPI)
2. Inetgrasi ke dashboard (streamlist, dash)
3. deploy ke cloud (AWS, Google Cloud, Azure)
4. bisa juga menggunakan Docker dengan tujuan supaya gampang dipindah pindah

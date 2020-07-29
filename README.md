# covid19-indonesian-tweet

Repository ini berisi kumpulan tweet yang berkaitan dengan COVID-19 sebagai bagian dari 
riset saya pada topik Social Media Analytics. Data yang tersedia untuk sementara waktu 
hanya dimulai dari tanggal 21 Juli 2020 akibat limit API Twitter yang hanya memperbolehkan 
nonpaid developer untuk mengambil tweet hingga satu minggu ke belakang.

## Deskripsi data

Setiap file merupakan file dalam format .csv dengan header {id} dan isinya berupa id tweet. 
Informasi seluruh tweet tidak dipublikasi untuk memenuhi 
[Terms of Service Twitter](https://developer.twitter.com/en/developer-terms/agreement-and-policy).

## Kriteria tweet

Tweet yang dikumpulkan harus teridentifikasi sebagai tweet berbahasa Indonesia dan bukan merupakan retweet. 
Selain itu, tweet juga memenuhi salah satu dari [keyword](./keywords.txt). Keywords yang digunakan 
merupakan hasil dari eksplorasi terms dan hashtags yang banyak muncul di dataset tweet berbahasa Indonesia
yang sebelumnya pernah dikumpulkan oleh PanaceaLab ([http://www.panacealab.org/covid19/]()) namun 
dengan keyword bahasa Inggris. Setelah ditemukan keyword dan hashtag yang paling banyak muncul di 
dataset tersebut, didefinisikan keyword dan hashtag baru yang relevan dengan situasi pandemi COVID-19
di Indonesia (misal: 'pandemi', 'penyebaran', '#dirumahaja'). Secara total, diperoleh 25 gabungan keyword
dan hashtag dari eksplorasi dataset tersebut.

## Hydrating

Untuk memperoleh data lengkap untuk setiap tweetnya, gunakan software Hydrator yang tersedia dalam 
format [GUI](https://github.com/DocNow/hydrator) dan [CLI (Python)](https://github.com/DocNow/twarc).

## Metode scraping

Scraper dijalankan secara berkala setiap harinya pada dini hari di Azure VM. Scraper akan mengumpulkan
semua tweet yang sesuai kriteria pada hari sebelumnya. Berikut adalah langkah scrapingnya:
1. Membuat koneksi ke API Twitter melalui AppAuth menggunakan Consumer Key dan Consumer Secret (dapat diperoleh di [https://developer.twitter.com/])
2. Melakukan scraping tweet secara iteratif (100 tweet/iterasi).
3. Pada setiap iterasi, tweet id di-append ke satu file.
4. Setelah proses scraping selesai (pada kondisi iterasi mengembalikan 0 tweet), 
file di-commit dan di-push ke repository GitHub.

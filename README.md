# covid19-indonesian-tweets

Status: **DISCONTINUED**

## English

This repository consists of a collection of Indonesian tweets related to COVID-19 as part of our research project. The collection started from July 21, 2020.

### Paper

This collection is a part of our paper in which the preprint can be accessed on https://arxiv.org/abs/2206.15359. Please cite this paper accordingly if you plan to use this dataset for your publications.

### Data Description

Each file is a comma-separated-values (CSV) file without header and contains a set of Tweet IDs. We only publish the tweet IDs to abide by the [Twitter's Terms of Service](https://developer.twitter.com/en/developer-terms/agreement-and-policy)

### Collected Tweet Criteria

The collected tweets fulfill a set of criteria, which are:
- Written in Indonesian
- Not a retweet (we aim for organic tweets)
- Contains at least one of the defined [COVID-19 keywords](./keywords.txt)

### How to Use

Following Twitter API's developer policy, we only publish the tweet IDs. *Hydrating* the tweet ID with the full data can be done by using available tools such as DocNow's hydrator (https://github.com/DocNow/hydrator) or by directly retrieving the data from Twitter API.

### How to Cite

#### Bibtex

```
@misc{faisal2022twostage,
      title={Two-Stage Classifier for COVID-19 Misinformation Detection Using BERT: a Study on Indonesian Tweets}, 
      author={Douglas Raevan Faisal and Rahmad Mahendra},
      year={2022},
      eprint={2206.15359},
      archivePrefix={arXiv},
      primaryClass={cs.CL}
}
```


## Indonesian

Repository ini berisi kumpulan tweet yang berkaitan dengan COVID-19 sebagai bagian dari 
riset kami. Data yang tersedia dimulai dari tanggal 21 Juli 2020.

### Deskripsi data

Setiap file merupakan file dalam format .csv dengan tanpa header dan isinya berupa ID tweet. 
Informasi seluruh tweet tidak dipublikasi untuk memenuhi 
[Terms of Service Twitter](https://developer.twitter.com/en/developer-terms/agreement-and-policy).

### Kriteria tweet

Tweet yang dikumpulkan memenuhi sekumpulan kriteria sebagai berikut:
- Ditulis dalam Bahasa Indonesia
- Bukan merupakan retweet (kami menargetkan *organic tweets*)
- Mengandung setidaknya salah satu [keyword COVID-19](./keywords.txt)

### Cara menggunakan data

Mengikuti developer policy milik Twitter API, kami hanya menerbitkan atribut tweet ID saja. Untuk memperoleh atribut lainnya dari sebuah tweet (atau yang dikenal dengan *hydrating*), Anda bisa menggunakan DocNow hydrator (https://github.com/DocNow/hydrator) atau dengan mengambil langsung melalui Twitter API.

### Sitasi

#### Bibtex

```
@misc{faisal2022twostage,
      title={Two-Stage Classifier for COVID-19 Misinformation Detection Using BERT: a Study on Indonesian Tweets}, 
      author={Douglas Raevan Faisal and Rahmad Mahendra},
      year={2022},
      eprint={2206.15359},
      archivePrefix={arXiv},
      primaryClass={cs.CL}
}
```

## License
<a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/">Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License</a>.

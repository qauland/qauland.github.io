---
layout: post
title:  "Ulas (Review) Apapun Menggunakan Mediumish!"
author: qauland
tags: [ selamat datang ]
image: https://source.unsplash.com/800x350/daily?book
description: "Ulas apa saja yang Anda inginkan menggunakan Mediumish."
featured: false
comments: true
rating: 3.5
last_modified_at: 2020-12-22
---

Buat artikel ulasan produk, buku, film, tempat wisata, dan apapun yang Anda sukai pada blog Jekyll Anda menggunakan [Mediumish](<https://www.wowthemes.net/mediumish-free-jekyll-template/>)! Anda bisa menggunakan *rating* 5-bintang pada artikel ulasan yang Anda tulis. *Rating* 5-bintang ini juga mendukung setengah bintang (mis. 3,5). *Rating* akan muncul di bagian bawah artikel dan di beranda.

## Caranya?

Mudah saja! Tambahkan `rating` pada bagian awal (*YAML front matter*) pos Anda.

```html
---
layout: post
title:  "Ulasan: Ascendance of a Bookworm"
author: tetew
categories: [ ulasan, review ]
tags: [ seri, animasi, televisi ]
image: assets/images/honzuki.jpg
description: "Ulasan saya terhadap Ascendance of a Bookworm, salah satu seri animasi televisi tahun 2019."
rating: 3.5
---
```

## Aku ingin mengulas buku/film/serial yang saya baca/tonton, tapi ulasanku mengandung *spoiler*!

Gunakan `<span class="spoiler">` untuk menyembunyikan *spoiler*. Contoh:

```html
*Spoiler*: <span class="spoiler">Myne berhasil membuat buku</span>
```

*Spoiler*: <span class="spoiler">Myne berhasil membuat buku</span>

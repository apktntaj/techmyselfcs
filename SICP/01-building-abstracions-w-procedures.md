# MEMBANGUNG ABSTRAKSI MELALUI PROCEDURES

Dalam membuat program, penting untuk membuatnya menjadi lebih modular.

Kenapa buku SICP memilih Lisp sebagai bahan ajar? karena fitur unik homoiconic. Homoiconic adalah sifat dari beberapa bahasa pemrograman di mana kode program dan data memiliki struktur yang sama. Ini berarti bahwa kode program dapat dimanipulasi sebagai data oleh program itu sendiri.

## The Elements of Programming

Bahasa yang powerful setidaknya memiliki tiga aspek berikut:

- primitive expressions
- means of combinations
- means of abstraction

Perbedaan antara ekspresi dan statement adalah ekspresi adalah baris kode yang selalu menghasilkan sebuah value sedangkan statement tidak selalu.

Selain prefix dan postfix notation, ada juga infix notation.

```scheme
; Prefix notation (Lisp)
(+ 1 2)

; Postfix notation (Forth)
1 2 +

; Infix notation (Python)
1 + 2
```

Keunggulanan dari _prefix notation_ adalah kesederhanaannya.

Dengan _prefix notation_ juga membuat kode di Lisp menjadi lebih natural dievaluasi.

Aturan mengevaluasi kode di Lisp sederhana. Evaluasi semua mulai dari kiri kode. Ada beberapa yang tidak mengikuti aturan ini. seperti `(define x 5)`. Kode tersebut tidak akan dievaluasi karena perintahnya hanya _binding_ nilai `5` ke varibel `x`. Pengecualian itu disebut _*special form*_. Di Lisp _special form_ lebih sedikit dibanding bahasa lain, itulah kenapa Lisp dianggap sebagai bahasa yang sederhana sintaksnya.

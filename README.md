# 3F-algoritmaPemrograman
Tentu, berikut template yang sama dengan masalah menentukan jenis segitiga berdasarkan panjang sisi.

Logika Matematika - Menentukan Jenis Segitiga
📝 Deskripsi Masalah

Dalam matematika, segitiga dapat dibedakan berdasarkan panjang sisi-sisinya. Segitiga dengan ketiga sisi yang sama panjang disebut segitiga sama sisi, segitiga dengan dua sisi yang sama panjang disebut segitiga sama kaki, sedangkan segitiga dengan ketiga sisi yang berbeda panjang disebut segitiga sembarang.

Masalah ini dapat digunakan untuk menerapkan logika matematika dalam menentukan jenis segitiga berdasarkan kondisi yang diberikan. Program akan menerima tiga panjang sisi segitiga sebagai input, kemudian membandingkan ketiga sisi tersebut. Berdasarkan hasil perbandingan, program akan menentukan jenis segitiga.

📥 Input-Proses-Output

Input: Tiga nilai panjang sisi segitiga, yaitu sisi A, sisi B, dan sisi C.

Proses: Program membandingkan panjang ketiga sisi:

Jika sisi A = sisi B dan sisi B = sisi C, maka segitiga adalah segitiga sama sisi.
Jika terdapat dua sisi yang sama panjang, maka segitiga adalah segitiga sama kaki.
Jika semua sisi memiliki panjang yang berbeda, maka segitiga adalah segitiga sembarang.

Output: Jenis segitiga berdasarkan panjang ketiga sisinya.

💻 Pseudocode
INPUT sisi_a
INPUT sisi_b
INPUT sisi_c

IF sisi_a == sisi_b AND sisi_b == sisi_c THEN
    OUTPUT "Segitiga sama sisi"
ELSE IF sisi_a == sisi_b OR sisi_a == sisi_c OR sisi_b == sisi_c THEN
    OUTPUT "Segitiga sama kaki"
ELSE
    OUTPUT "Segitiga sembarang"
END IF

📊 Flowchart
%%{init: {
  "themeVariables": {
    "fontSize": "12px"
  },
  "flowchart": {
    "nodeSpacing": 15,
    "rankSpacing": 20,
    "padding": 8
  }
}}%%

flowchart TD
    A([START]) --> B[/INPUT sisi A, sisi B, sisi C/]
    B --> C{Apakah A = B<br/>dan B = C?}

    C -->|Ya| D[/OUTPUT<br/>"Segitiga sama sisi"/]
    C -->|Tidak| E{Apakah A = B<br/>atau A = C<br/>atau B = C?}

    E -->|Ya| F[/OUTPUT<br/>"Segitiga sama kaki"/]
    E -->|Tidak| G[/OUTPUT<br/>"Segitiga sembarang"/]

    D --> H([END])
    F --> H
    G --> H

    style A fill:#dbeafe,stroke:#2563eb,stroke-width:2px,color:#1e3a8a
    style B fill:#dcfce7,stroke:#16a34a,stroke-width:2px,color:#14532d
    style C fill:#fef3c7,stroke:#d97706,stroke-width:2px,color:#78350f
    style D fill:#dcfce7,stroke:#16a34a,stroke-width:2px,color:#14532d
    style E fill:#fef3c7,stroke:#d97706,stroke-width:2px,color:#78350f
    style F fill:#e0e7ff,stroke:#4f46e5,stroke-width:2px,color:#312e81
    style G fill:#fee2e2,stroke:#dc2626,stroke-width:2px,color:#7f1d1d
    style H fill:#dbeafe,stroke:#2563eb,stroke-width:2px,color:#1e3a8a

🧪 Test Case
Test Case	Input Sisi A	Input Sisi B	Input Sisi C	Kondisi	Hasil yang Diharapkan
1	5	5	5	A = B = C	Segitiga sama sisi
2	5	5	3	A = B	Segitiga sama kaki
3	4	5	6	A ≠ B ≠ C	Segitiga sembarang
🐍 Implementasi Python

Implementasi program dibuat menggunakan Python dan dijalankan melalui Visual Studio Code.
Source code dapat dilihat pada main.py.

sisi_a = int(input("Masukkan sisi A: "))
sisi_b = int(input("Masukkan sisi B: "))
sisi_c = int(input("Masukkan sisi C: "))

if sisi_a == sisi_b and sisi_b == sisi_c:
    print("Segitiga sama sisi")
elif sisi_a == sisi_b or sisi_a == sisi_c or sisi_b == sisi_c:
    print("Segitiga sama kaki")
else:
    print("Segitiga sembarang")

📸 Hasil Pengujian

Program telah berhasil diuji menggunakan tiga kombinasi panjang sisi, yaitu (5, 5, 5), (5, 5, 3), dan (4, 5, 6) sesuai dengan test case. Program menghasilkan segitiga sama sisi untuk input pertama, segitiga sama kaki untuk input kedua, dan segitiga sembarang untuk input ketiga. Hasil tersebut sesuai dengan kondisi yang telah ditentukan.

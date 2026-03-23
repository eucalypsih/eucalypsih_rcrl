# eucalypsih_rcrl

# Kata Ganti (Pronouns)
* Kata ganti orang (I, you, he, she, it, we, they)
* Kata ganti kepemilikan (mine, yours, his, hers, ours, theirs)
* Kata ganti objek (me, you, him, her, us, them)

# Tenses (Waktu dalam Kalimat)
* Present tense (Sekarang)
* Past tense (Lampau)
* Future tense (Akan datang)
* Continuous tense (Sedang berlangsung)
* Perfect tense (Sudah selesai)

# Kata Kerja (Verbs)
* Kata kerja dasar (walk, eat, run)
* Kata kerja bantu (be, have, do)
* Kata kerja tidak beraturan (go - went, see - saw)
* Kata kerja modal (can, could, will, would, should)

# Kalimat dan Struktur Kalimat
* Kalimat afirmatif, negatif, dan tanya
* Penggunaan subjek, predikat, objek
* Kalimat kompleks dan sederhana

# Kata Benda (Nouns)
* Kata benda umum dan khusus
* Kata benda tunggal dan jamak
* Kata benda abstrak dan konkret

# Kata Sifat (Adjectives)
* Penggunaan untuk mendeskripsikan benda/noun
* Perbandingan (better, best)
* Derivasi kata sifat

# Kata Keterangan (Adverbs)
* Menjelaskan kata kerja, kata sifat, atau kata keterangan lain
* Tempat, waktu, frekuensi, cara



* tidak banyak memerlukan biaya.
* tidak memerlukan banyak biaya.
* it doesn't require much cosh

singular (myself, yourself, himself, herself, itself)
(self-esteem, self-control)
> buatkan diagram visual kecil yang menunjukkan hubungan “self” → myself / yourself / himself / themselves, sehingga lebih mudah diingat. Ini biasanya bikin belajar reflexive pronoun jadi super jelas.

subjek=i
word=myself
ket

subjek=it
word=itself
ket=Kata ini adalah bentuk refleksif dari "it".
keg=Menunjukkan bahwa subjek dan objek adalah sama, biasanya untuk benda atau hewan.

subjek=he
word=himself
keg=Menunjukkan bahwa tindakan dilakukan oleh subjek terhadap dirinya sendiri.

> buatkan versi diagram super warna-warni yang benar-benar “eye-catchy” ala poster belajar bahasa Inggris, sehingga tinggal ditempel di dinding atau layar HP untuk menghafal reflexive pronouns dalam 5 detik.

> buatkan versi diagram di source code program python super warna-warni yang benar-benar “eye-catchy” ala poster belajar bahasa Inggris, sehingga tinggal di jalankan atau run HP untuk menghafal reflexive pronouns dalam 5 detik.

tkinter-exclude
```python
import time
import random
import sys

# Daftar reflexive pronouns
pronouns = ["myself", "yourself", "himself", "herself", "itself", "ourselves", "yourselves", "themselves"]

# Contoh kalimat
examples = [
    "I made myself a sandwich.",
    "She looked at herself in the mirror.",
    "They enjoyed themselves at the party.",
    "He hurt himself while working.",
    "We prepared ourselves for the test."
]

# Fungsi untuk mendapatkan warna acak menggunakan ANSI escape codes
def get_color_code():
    return f"\033[38;5;{random.randint(16, 231)}m"

# Fungsi untuk menampilkan teks berwarna-warni secara bergantian
def print_color_cycle(texts, delay=0.3):
    for i in range(10):  # Loop beberapa kali agar warna berganti
        for text in texts:
            color = get_color_code()
            sys.stdout.write(f"{color}{text}\033[0m\n")
            sys.stdout.flush()
            time.sleep(delay)

# Tampilkan judul
print("\n" + "="*50)
print("\033[1;35m🌟 BELAJAR REFLEXIVE PRONOUNS 🌟\033[0m")
print("Tinggal jalankan dan hafalkan dalam 5 detik!\n")
print("="*50 + "\n")

# Tampilkan daftar reflexive pronouns dengan warna-warni
print("Daftar Reflexive Pronouns:\n")
print_color_cycle(pronouns, delay=0.3)

# Tampilkan contoh kalimat dengan warna-warni
print("\nContoh Kalimat:\n")
print_color_cycle(examples, delay=0.3)

# Tunggu selama 5 detik
time.sleep(5)

# Selesai
print("\nSelesai! Semoga bermanfaat! 🚀")

```

tkinter-included
```python
import tkinter as tk
import random

# Fungsi untuk mengganti warna secara acak
def random_color():
    return "#" + "".join([random.choice('0123456789ABCDEF') for _ in range(6)])

# Fungsi untuk menampilkan teks dengan warna-warni secara bergantian
def color_cycle(label, texts, delay=300):
    def update(index=0):
        label.config(text=texts[index % len(texts)], fg=random_color())
        label.after(delay, update, index+1)
    update()

# Membuat window utama
root = tk.Tk()
root.title("Belajar Reflexive Pronouns")
root.geometry("600x400")
root.configure(bg='black')

# Judul utama
title = tk.Label(root, text="🌟 Belajar Reflexive Pronouns 🌟", font=("Comic Sans MS", 24, "bold"), bg='black')
title.pack(pady=10)

# Penjelasan singkat
desc = tk.Label(root, text="Tinggal jalankan dan hafalkan dalam 5 detik!", font=("Arial", 14), bg='black')
desc.pack(pady=5)

# Daftar reflexive pronouns
pronouns = ["myself", "yourself", "himself", "herself", "itself", "ourselves", "yourselves", "themselves"]
pronoun_label = tk.Label(root, text="", font=("Arial", 18, "bold"))
pronoun_label.pack(pady=10)

# Contoh kalimat
examples = [
    "I made myself a sandwich.",
    "She looked at herself in the mirror.",
    "They enjoyed themselves at the party.",
    "He hurt himself while working.",
    "We prepared ourselves for the test."
]
example_label = tk.Label(root, text="", font=("Arial", 16), wraplength=550, justify='center')
example_label.pack(pady=10)

# Mulai efek warna-warni
color_cycle(pronoun_label, pronouns, delay=300)
color_cycle(example_label, examples, delay=300)

# Tutup otomatis setelah 5 detik
root.after(5000, root.destroy)

root.mainloop()

```

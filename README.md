# Stegano-OTP

Steganografi adalah seni atau ilmu yang berhubungan dengan menyembunyikan pesan atau data dalam suatu media tanpa meninggalkan jejak bahwa pesan tersebut disembunyikan. Salah satu bentuk steganografi yang umum digunakan adalah steganografi pada gambar, di mana pesan atau data disisipkan ke dalam gambar sehingga tampak seperti gambar tersebut tidak mengandung informasi tersembunyi.

Sementara itu, One-Time Pad (OTP) adalah suatu metode enkripsi yang menggunakan kunci sepanjang pesan, di mana kunci hanya digunakan sekali dan tidak dapat diprediksi. Jika OTP diterapkan dengan benar, pesan yang dienkripsi dengan OTP dianggap aman dan tidak dapat dipecahkan, asalkan kunci tidak pernah digunakan lebih dari satu kali.

<h2>Fungsi OTP yg digunakan</h2>

<b>Fungsi untuk mengenkripsi teks menggunakan One-Time Pad (OTP)</b>
```
def otp_encrypt(plain_text, key):
    encrypted_text = ''
    for i in range(len(plain_text)):
        char = plain_text[i]
        key_char = key[i % len(key)]
        encrypted_text += chr(ord(char) ^ ord(key_char))
    return encrypted_text
```
<b>Fungsi untuk mengonversi teks ke dalam bentuk biner</b>
```
def text_to_binary(text):
    binary_data = ''.join(format(ord(char), '08b') for char in text)
    return binary_data
```



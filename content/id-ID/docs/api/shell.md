# kulit

> Kelola file dan URL menggunakan aplikasi bawaan mereka.

Proses:  Utama </ 0> ,  Renderer </ 1></p> 

The `shell` modul menyediakan fungsi yang berkaitan dengan integrasi desktop.

Contoh membuka URL di browser default pengguna:

```javascript
const {shell} = require('electron') shell.openExternal ('https://github.com')
```

## Metode

The `shell` modul memiliki metode berikut:

### `shell.showItemInFolder (fullPath)`

* `fullPath` String

Mengembalikan `Boolean` - Apakah item berhasil ditampilkan

Tampilkan file yang diberikan di file manager. Jika memungkinkan, pilih file.

### `shell.openItem (fullPath)`

* `fullPath` String

Mengembalikan `Boolean` - Apakah item berhasil dibuka.

Buka file yang diberikan dengan cara default desktop.

### `shell.openExternal (url [, pilihan, callback])`

* ` url </ 0> String</li>
<li><code>pilihan` Objek (opsional) *macOS* 
  * `Aktifkan` Aljabar Boolean - `benar` untuk membawa aplikasi dibuka latar depan. Default adalah `benar`.
* `callback` Fungsi (opsional) - Jika ditentukan akan tampil terbuka secara asinkron. *macOS* 
  * ` error </ 0> Kesalahan</li>
</ul></li>
</ul>

<p>Mengembalikan <code>Boolean` - Apakah sebuah aplikasi tersedia untuk membuka URL. Jika callback ditentukan, selalu mengembalikan true.</p> 
    Buka URL protokol eksternal yang diberikan dengan cara default desktop. (Misalnya, mailto: URL di agen email default pengguna).
    
    ### `shell.moveItemUntukSampah(JalurPenuh)`
    
    * `fullPath` String
    
    Kembali `Boolean` - Apakah item berhasil dipindahkan ke tempat sampah
    
    Pindahkan file yang diberikan ke sampah dan mengembalikan status boolean untuk pengoperasiannya.
    
    ### `Shell.beep()`
    
    Bermain suara bip.
    
    ### `shell.writeShortcutLink (shortcutPath [, operasi], pilihan)` *Windows*
    
    * `shortcutPath` String
    * `operasi` String (opsional) - Default adalah `membuat`, bisa jadi salah satu dari berikut ini: 
      * `buat` - membuat shortcut baru, Timpa jika diperlukan.
      * `update` - update ditentukan properti hanya pada tombol cepat yang ada.
      * `menggantikan` - menimpa tombol cepat yang ada, gagal jika tidak ada jalan pintas.
    * `pilihan` [ShortcutDetails](structures/shortcut-details.md)
    
    Kembali `Boolean` - Apakah cara pintas telah dibuat berhasil
    
    Membuat atau memperbarui tautan pintasan di `shortcutPath`.
    
    ### `shell.readShortcutLink(shortcutPath)` *Windows*
    
    * `shortcutPath` String
    
    Kembali [`ShortcutDetails`](structures/shortcut-details.md)
    
    Menyelesaikan link pintasan di `shortcutPath`.
    
    Pengecualian akan dilemparkan ketika terjadi kesalahan.
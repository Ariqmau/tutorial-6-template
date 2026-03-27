# Tutorial 6 - Menu & In-Game GUI

Berikut adalah penjelasan singkat mengenai implementasi fitur-fitur pada tutorial ini:

### 1. Tombol Game Over ke Main Menu
Pada scene `Game Over.tscn`, ditambahkan tombol untuk kembali ke layar utama. Sinyal `pressed()` pada tombol dihubungkan ke fungsi yang memanggil `get_tree().change_scene_to_file("res://scenes/MainMenu.tscn")`.

### 2. Tombol Win Screen ke Main Menu
Pada scene `Win Screen.tscn`, tombol "Back to Main Menu" diimplementasikan dengan logika yang sama, menggunakan sinyal `pressed()` untuk mengarahkan pemain kembali ke menu utama setelah berhasil menyelesaikan permainan.

### 3. Fitur Select Stage
Scene `SelectStage.tscn` dibuat sebagai menu pemilihan level. Tombol-tombol pada menu ini memanfaatkan script yang memiliki variabel `@export var scene_to_load: String`. Hal ini memungkinkan penentuan tujuan level (seperti "Level 1" atau "Level 2") diatur langsung melalui panel Inspector editor Godot.

### 4. Transisi Antar Level (Level 1 ke Level 2)
Perpindahan dari Level 1 ke Level 2 menggunakan scene perantara bernama `NextLevel.tscn`. Ketika pemain menyentuh area pemicu di akhir Level 1, permainan akan memuat layar `NextLevel.tscn` sebagai jeda atau transisi, sebelum pemain akhirnya melanjutkan ke `Level 2.tscn`.
### Latihan: Playtest
### 1. Apa saja pesan log yang dicetak pada panel Output? 
Jawab: "Platform initialized" - pesan ini muncul saat permainan dimulai untuk memberi tahu bahwa platform sudah siap digunakan.

### 2. Coba gerakkan landasan ke batas area bawah, lalu gerakkan kembali ke atas hingga hampir menyentuh batas atas. Apa saja pesan log yang dicetak pada panel Output?
Jawab: "Reached objective!" - pesan ini muncul ketika kapal biru berhasil mencapai area tujuan yang berada di bagian atas permainan.

### 3. Buka scene MainLevel dengan tampilan workspace 2D. Apakah lokasi scene ObjectiveArea memiliki kaitan dengan pesan log yang dicetak pada panel Output pada percobaan sebelumnya?
Jawab: Ya, sangat berkaitan. ObjectiveArea adalah area target yang ditempatkan di bagian atas permainan. Ketika kapal biru menyentuh area ini, maka pesan "Reached objective!" muncul di panel Output. Jadi lokasi ObjectiveArea adalah tempat yang harus dicapai untuk menyelesaikan misi.


### Latihan: Memanipulasi Node dan Scene
### 1. Scene BlueShip dan StonePlatform sama-sama memiliki sebuah child node bertipe Sprite2D. Apa fungsi dari node bertipe Sprite2D?
Jawab: Sprite2D berfungsi untuk menampilkan gambar di layar. Ini adalah yang membuat kita bisa melihat visual dari kapal biru atau batu di permainan.

### 2. Root node dari scene BlueShip dan StonePlatform menggunakan tipe yang berbeda. BlueShip menggunakan tipe RigidBody2D, sedangkan StonePlatform menggunakan tipe StaticBody2D. Apa perbedaan dari masing-masing tipe node?
Jawab: 
- RigidBody2D (BlueShip): Ini adalah benda yang bisa bergerak dan jatuh karena gravitasi, seperti benda nyata di dunia fisika. Kapal biru bisa bergerak ke atas dan bawah.
- StaticBody2D (StonePlatform): Ini adalah benda yang tetap diam dan tidak bergerak, seperti tanah atau platform. Fungsinya adalah tempat untuk benda lain berdiri atau menumpu.

### 3. Ubah nilai atribut Mass pada tipe RigidBody2D secara bebas di scene BlueShip, lalu coba jalankan scene MainLevel. Apa yang terjadi?
Jawab: Mass menentukan seberapa berat kapal biru terasa:
- Mass lebih besar: Kapal terasa lebih berat, jatuh lebih cepat, dan lebih sulit untuk digerakkan.
- Mass lebih kecil: Kapal terasa lebih ringan, jatuh lebih lambat, dan lebih mudah untuk digerakkan.

### 4. Ubah nilai atribut Disabled milik node CollisionShape2D pada scene StonePlatform, lalu coba jalankan scene MainLevel. Apa yang terjadi?
Jawab: 
- Jika Disabled diatur ke true (aktif): Platform batu menjadi "hantu" - kapal biru bisa jatuh menembus platform tanpa hambatan.
- Jika Disabled diatur ke false (tidak aktif): Platform batu menjadi solid - kapal biru bisa mendarat dan menumpu di atasnya.

### 5. Pada scene MainLevel, coba manipulasi atribut Position, Rotation, dan Scale milik node BlueShip secara bebas. Apa yang terjadi pada visualisasi BlueShip di Viewport?
Jawab:
- Position: Menggeser lokasi kapal di layar ke arah mana saja.
- Rotation: Memutar kapal sehingga menghadap ke arah yang berbeda.
- Scale: Mengubah ukuran kapal, bisa membuat lebih besar atau lebih kecil.

### 6. Pada scene MainLevel, perhatikan nilai atribut Position node PlatformBlue, StonePlatform, dan StonePlatform2. Mengapa nilai Position node StonePlatform dan StonePlatform2 tidak sesuai dengan posisinya di dalam scene (menurut Inspector) namun visualisasinya berada di posisi yang tepat?
Jawab: StonePlatform dan StonePlatform2 adalah anak dari PlatformBlue, jadi posisi mereka ditampilkan relatif terhadap parent-nya. Nilai di Inspector adalah posisi lokal mereka saja, tetapi posisi di layar adalah posisi lokal ditambah posisi parent. Itu sebabnya posisi di Inspector berbeda dengan yang terlihat di layar - layar menunjukkan posisi absolut (lengkap), sedangkan Inspector menunjukkan posisi relatif terhadap parent.
# Advanced Programming - Tutorial Modul 10
## Daniel Ferdiansyah, 2306275052

### Experiment 1.2

![image](https://github.com/user-attachments/assets/449816bb-039c-4de7-9024-4ed9743ca510)

Output yang pertama kali muncul adalah `Daniel's Computer: hey hey`. Hal ini karena line code tersebut dieksekusi secara synchronus, sehingga akan langsung muncul ketika fungsi `main` dieksekusi.
Lalu, segera setelah task asynchronus dieksekusi, `Daniel's Computer: howdy!` muncul. Setelah 2 detik (menandakan kalau Future selesai), maka akan muncul `Daniel's Computer: done!`.

### Experiment 1.3

![image](https://github.com/user-attachments/assets/58bab235-1ac5-428e-95ee-ebdd213a5985)

Setelah menggandakan spawn jadi 3, terlihat bahwa proses asynchronus juga berjalan tiga kali. Pertama, `howdy!` dieksekusi baik 1, 2, dan 3. Lalu, `done!` juga dieksekusi baik 1, 2, dan 3.

![image](https://github.com/user-attachments/assets/097a9cdc-a7d1-4699-b2dd-ee19ce00d875)

Lalu, ketika `drop(spawner)` dihilangkan, maka executor tidak pernah selesai menjalankan task asynchronusnya. Hal ini menyebabkan program masuk dalam kondisi *deadlock*. Jadi program tidak akan berhenti kecuali di-*terminate* paksa.

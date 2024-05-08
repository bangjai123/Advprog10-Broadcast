# Reflection

##### Nama: Zaidan Naufal Ilmi
##### Kelas: Adpro-A
##### NPM: 2206081761

<details>
  <summary>Experiment 2.1: Original code, and how it run</summary>

  ![image](https://github.com/bangjai123/Advprog10-Broadcast/assets/120235144/d91a1c61-145c-4411-9a2d-8d0f2f57acf1)

Pada gambar di atas, terdapat 4 terminal yang dibuka. Terminal kiri atas digunakan untuk menjalankan server dengan perintah `cargo run --bin server` dan sisanya berperan sebagai client dengan menggunakan perintah `cargo run --bin client`. Ini adalah simulasi broadcast. Pada saat salah satu client mengirimkan pesan, server menerimanya dan meneruskannya ke semua client yang lain. Dengan demikian, pesan yang ditulis di salah satu client akan muncul di client-client yang lainnya. 

</details>

<details>
  <summary>Experiment 2.2: Modifying port</summary>

  ![image](https://github.com/bangjai123/Advprog10-Broadcast/assets/120235144/56ebb017-a83d-49b8-8c8f-3901875769dd)
  
Untuk mengubah port web socket menjadi 8080, kita perlu memodifikasi file client.rs dan server.rs. Pada client.rs, kita perlu mengubah `ClientBuilder::from_uri(Uri::from_static("ws://127.0.0.1:2000"))` menjadi       `ClientBuilder::from_uri(Uri::from_static("ws://127.0.0.1:8080"))`. Lalu, pada server.rs, kita perlu mengubah `    let listener = TcpListener::bind("127.0.0.1:2000").await?;` menjadi `let listener = TcpListener::bind("127.0.0.1:8080").await?;`. Hal ini dilakukan karena keduanya perlu terhubung ke port yang sama. Dengan demikian, port keduanya perlu diubah menjadi 8080.

</details>

# Week3_2-Migration-Users-dan-KHS

Untuk memulai materi migration , siapkan beberapa tools berikut :
1. XAMPP / SQLyog
2. VsCode / IDE yang lain

Langkah-langkah sebelum membuat migration:
1. Buat folder service-user
2. Buka terminal lalu masuk ke folder service-user dengan perintah CD(change directory)
3. Jika sudah ketikkan perintah-perintah berikut :
    1) npx express-generator --no-view (Jika tidak ingin menggunakan view)
    2) npm i 
    3) npm i nodemon
    4) npm dotenv --save
    5) npm i --save sequelize sequelize-cli
    6) npx sequelize init (Berfungsi untuk memunculkan folder default dari sequelize)
    7) npm i mysql2 --save
    
Jika sudah, waktunya membuat migration. Berikut ini adalah cara membuat migration:
    1) Buat file .env di folder yang sama seperti file app.js. Pada file .env isikan sesuai pada file di repository.
    2) Rename file config.json yang ada pada folder config menjadi config.js dan edit seperti file config.js yang ada pada repository.
    3) Edit file index.js pada folder models, edit sesuai file index.js di repository ini (ada di folder models juga).
    4) Edit file app.js seperti pada file app.js diatas.
    5) Pada terminal ketikkan npx sequelize migration:create --name=(nama file migration) -> create-table-users yang nantinya berfungsi untuk membuat file migration untuk tabel users 
    6) Pada terminal ketikkan npx sequelize migration:create --name=(nama file migration) -> create-table-khs yang nantinya berfungsi untuk membuat file migration untuk tabel khs
    7) Isi kedua file migration seperti pada file yang ada di folder migrations i repository ini.
    8) Jika sudah hidupkan xampp/mysql dan buat database dengan nama service_users
    9) Selanjutnya ketikkan npx sequelize db:migrate untuk membuat table di database dengan migrate

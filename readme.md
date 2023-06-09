# React Authentication With Phyton and Jwt

## Feature Login

    Todo:
    1.  package Install
        - cd react-auth : npm i react-router-dom axios bootstrap
    2.  components/Navbar.jsx
        - functional Navbar
    3.  Login.jsx
        - functional Login
        - deklarasi hooks
        - pasang handleLogin
        - pasang setLoading untuk button
        - inisialisasi  user dan token  agar lebih dipanggil
    4.  components/Home.jsx
        - functional Home
        - import dan pasang Navbar & Footer
    4.  components/Footer.jsx
        - functional component footer
    5.  main.jsx
        - pasang bootstrap
    6.  index.css
        - pasang bootstra
    7.  App.jsx
        - import dan pasang Login dan Home
    8.  jalankan app : cd frontend/npm run dev

## Feature Register

    Todo:
    1.  Register
        - copas code dari Login kemudian modifikasi form
        - deklarasi hooks register
        - animation loading
        - pasang use navigate
        - handleChangeInput
        - handleRegister
        - import dan pasang Navbar & Footer
    2.  App.js
        - import dan pasang path Register
    3.  pengujian pada browser:
        - klik menu register
          akan diarahkan kehalaman : http://localhost:5173/register
        - lakukan pengisian form register dan klik button egister
        - jika setup yang kita lakukan berhasil akan diarahkan kehalaman homepage

## isLoggedIn & menampilkan nama user yang login

    Todo:
    1.  Navbar
        - memasang hooks
        - useEffect untuk mengechek jikasudah login apa belum
        - pasang logig isLoggedIn pada menu (profile dam username)
        - menampilkan data user yang login dengan mencetak namanya : {user.name}
    2.  pengujian pada browser:
        - klik menu login
          akan diarahkan kehalaman : http://localhost:5173/login
        - lakukan pengisian form login dengan username dan password yang terdaftar dan klik button login
        - jika setup yang kita lakukan berhasil akan diarahkan kehalaman homepage

## Logout

    Todo:
    1.  Navbar
        - handleLogout
    2.  pengujian pada browser:
        - setelah behasil login klik dropdown menu lalu klik logout
        - jika setup yang kita lakukan berhasil akan menampilkan button login dan register

## Profile Page

    Todo:
    1.  components/Navbar.jsx
        - pasang path '/profile'
    2.  components/Profile.jsx
        - functional component Profile
        - pasang deault endpoint
        - hooks profile
        - useEffect menampilkan data profile
        - pasang token yang login
        - buat kondisi jika gambar  ada dan tidak ada pada database
    3.  App.jsx
        - import dan pasang Profile path
    4.  auth/Login.jsx
        - redirect to profile dengan useNavigate()
    5.  pengujian pada browser:
        - setelah behasil login
        - jika setup yang kita lakukan berhasil akan akan ter-redirect ke halaman profile

## Penggunaan Middleware untuk Proteksi Halaman pada ReactJS

    Todo:
    1.  components/Profile.jsx
        - hooks authentication
        - pasang authenticated
        - tampilan untuk yang memaksa mengakses profile
        - import dan pasang NotAuthor
    2.  components/NotAuthor.jsx
        - functional NotAuthor
    3.  auth/Login.jsx
        - hadnle ketika user sudah login tidak bisa akses halaman login
    4.  pengujian pada browser:
        - setelah behasil logout coba akses halaman profile : http://localhost:5173/profile
        - jika setup yang kita lakukan berhasil akan akan tanpil page NotAuthorize

## Handle data kosong dan tidak valid pada Login

    Todo:
    1.  install Toastify
        - npm i react-toastify
        - docs : https://www.npmjs.com/package/react-toastify
    2.  App.jsx
        - import dan pasang ToastifyContainer
        - docs toastify : https://fkhadra.github.io/react-toastify/introduction/
    3.  auth/Login.jsx
        - buat validasi username and password
            * panggil fungsi validasi
            * pasang setLoading untuk button bernilai true
        - penambahan code untuk data yang tidak valid
            * jika kesalahan berasal dari API & bukan dari username & password
            * pasang setLogin ketika user salah memasukan email atau password
    4.  pengujian pada browser:
        - pada halaman login: http://localhost:5173/login
        - kosongkan form dan lakukan klik login, jika setup yang kita buat berhasil
          akan ada notifkasi Please enter a Username & Please enter a Password
        - jika salah satu di isi trus tekan login maka yang tidak teisi tersebut muncul di pesan toastify
        - jika data yang dimasukan tidak sama dengan di database akan ada notifikasi invalid username or password

## Handle user access path register setelah berhasil login

    Todo:
    1.  auth/Register.jsx
        - handle ketika user sudah login tidak bisa masuk kehalaman Reegister
    2.  pengujian pada browser:
        - ketika sudah login, coba akses halaman register: http://localhost:5173/register
        - jika setup yang kita lakukan berhasil akan di redirect ke halaman home

## Title pada setiap halaman

    Todo:
    1.  auth/Register.jsx
        - title Register
    2.  auth/login.jsx
        - title Login
    3.  components/Profile.jsx
        - stitle profile = set document title to 'Profile' + name
    4.  components/NotAuthor.jsx
        - title NotAuthorize!
    5.  pengujian pada browser:
        - klik register => nama title Register
        - klik login => nama title Login
        - klik profile => nama title Profile + nama user yang login

## Menu active stiap halaman & memasang toastify

    Todo:
    1.  components/Navbar.jsx
        - pasang usLocation dari react-router-dom
        - gunakan location untuk menu home & profile
        - pasang toastify
    2.  auth/Login.jsx
        - pasang toastify

## Desain halaman home & login

    Todo:
    1.  components/Home.jsx
        - design home
    2.  auth/Login.jsx
        - design logini

## User page

    Todo:
    1.  components/Users.jsx
        - table users
    2.  App.jsx
        - import dan pasang Users
    3.  Navbar.jsx
        - pasang menu users
    4.  pengujian pada browser:
        setelah berhasil login klik menu users, akan diarahkan ke page users
        jika setup yang kita lakukan berhasil data seluruh users akan tampil
        pada tabel users

## Search users

    Todo:
    1.  components/Users.jsx
        - hooks untuk seacrh
        - pasang on change
        - pasang filter
    2. Pengujian pada browser:
        - setelah berhasil login klik menu users, akan diarahkan ke page users
          dana seluruh users akan tampil pada tabel users,
        - kemudian coba masukan nama pada serach, jika setup yang kita lakukan
          berhasil maka nama yang dicari akan tampil.

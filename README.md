# Pemrograman Lanjut A
> Fadrian Yhoga Pratama - 2206819395

## Module 5 - Java Profiling
### Reflection 
1. **Performance Testing** dengan **JMeter** dan **profiling** dengan **IntelliJ Profiler** memiliki peran yang berbeda dalam mengoptimalkan kinerja aplikasi.

    **Performance Testing dengan JMeter**:
    - **Tujuan**: Memastikan aplikasi berfungsi sesuai dengan *service level agreements* (SLA) di bawah berbagai jenis beban.
    - **Metode**: Menjalankan skenario pengujian dengan beban yang berbeda (misalnya, banyak pengguna, permintaan tinggi) untuk mengukur respons aplikasi.
    - **Hasil**: Mengidentifikasi masalah kinerja seperti *bottleneck*, *scalability*, dan *throughput*.
    - **Contoh**: Memastikan aplikasi web dapat menangani 1000 pengguna secara bersamaan.

    **Profiling dengan IntelliJ Profiler**:
    - **Tujuan**: Memahami perilaku kode Java pada saat runtime.
    - **Metode**: Mengumpulkan data tentang eksekusi program tanpa mengganggu program yang sedang berjalan.
    - **Hasil**: Menemukan *hot spots*, alokasi memori, dan pemanggilan fungsi yang mempengaruhi kinerja.
    - **Contoh**: Mengidentifikasi bagian kode yang memakan waktu eksekusi terbanyak.

    Keduanya memiliki peran penting dalam mengoptimalkan aplikasi, dengan JMeter fokus pada pengujian sistem secara keseluruhan, sementara IntelliJ Profiler memberikan wawasan mendalam tentang perilaku kode pada level yang lebih detail.

2. Proses profiling membantu dalam mengidentifikasi dan memahami titik lemah dalam aplikasi dengan menganalisis metrik kinerjanya, seperti penggunaan CPU, konsumsi memori, dan waktu eksekusi. Melalui profiling, dapat diidentifikasi bottleneck, algoritma yang tidak efisien, atau operasi yang memakan banyak sumber daya yang berkontribusi pada kinerja yang kurang optimal.
3. Ya, IntelliJ Profiler adalah alat yang efektif untuk membantu menganalisis dan mengidentifikasi bottleneck dalam kode aplikasi. Alat ini menyediakan berbagai fitur yang memungkinkan pengguna untuk memantau penggunaan CPU, alokasi memori, waktu eksekusi, dan kinerja jaringan. Dengan informasi yang diberikan oleh IntelliJ Profiler, saya dapat dengan cepat mengidentifikasi bagian dari kode yang menyebabkan kinerja buruk dan mengambil langkah-langkah untuk mengoptimalkannya
4. Beberapa tantangan yang saya hadapai dalam melakukan _Performance Testing_ dan _Profiling_ adalah:
    - Membaca Flame Graph, bottlenecks, Method list, dll pada intelliJ
    - Melakukan Optimisasi juga merupakan tantangan untuk saya karena apabila bottleneck telah ditemukan, saya harus segera melakukan _refactoring_ pada _bottleneck_ tersebut agar performa aplikasi saya menjadi lebih baik
5. Beberapa manfaat yang diperoleh dari penggunaan **IntelliJ Profiler** adalah memudahkan proses **profiling** dengan integrasi yang kuat antara **IDE** dan **Profiler**. _Ineterface_ yang bisa dibilang **user-friendly** juga membantu dalam memahami hasil evaluasi yang telah dilakukan. Informasi tentang **CPU Time**, **Total Time**, dan **Memory Management** yang diberikan oleh **IntelliJ Profiler** dapat dimanfaatkan oleh para developer untuk melakukan **optimasi kode**
6. Saya sendiri belom pernah mengalami masalah inkonsistensi dari IntelliJ Profiler dan JMeter. Namun, apabila saya menghadapi situasi tersebut, langkah yang saya ambil adalah memeriksa ulang konfigurasi yang telah saya lakukan pada JMeter dan mengevaluasi hasil profiling yang saya peroleh dari IntelliJ Profiler. Jika masih terjadi ketidaksesuaian, saya akan mencari solusinya di mesin pencarian seperti Google, OperaGX, dll atau bisa bertanya melalui teman dan asdos.
7. Setelah menganalisis hasil performance testing dan profiling, berikut adalah strategi yang saya lakukan untuk mengoptimalkan kode aplikasi:
    - Melihat hasil profiling pada method mana yang memakan waktu banyak dan tidak efisien
    - Memahami kode yang harus dioptimalkan
    - Memilih dan menggunakan algoritma dan struktur data yang paling efektif untuk memperbaiki method tersebut
    - Melakukan testing ulang menggunakan performance testing untuk memastikan bahwa perbaikan telah berhasil dan tidak memperkenalkan masalah baru

## JMeter Report and Test Results
### Jmeter GUI Test Result (Before and After Optimization)
- `/all-student`
  - Before
  ![all-student-before.jpg](src%2Fimg%2Fall-student-before.jpg)
  - After
  ![all-student-after.jpg](src%2Fimg%2Fall-student-after.jpg)
- `/all-student-name`
  - Before
  ![all-student-name-before.jpg](src%2Fimg%2Fall-student-name-before.jpg)
  - After
  ![all-student-name-after.jpg](src%2Fimg%2Fall-student-name-after.jpg)
- `/highest-gpa`
  - Before
  ![highest-gpa-before.jpg](src%2Fimg%2Fhighest-gpa-before.jpg)
  - After
  ![highest-gpa-after.jpg](src%2Fimg%2Fhighest-gpa-after.jpg)

### Jmeter Command Line Test Result
- `/all-student`
![ts1.jpg](src%2Fimg%2Fts1.jpg)
- `/all-student-name`
![ts2.jpg](src%2Fimg%2Fts2.jpg)
- `/highest-gpa`
![ts3.jpg](src%2Fimg%2Fts3.jpg)

Dapat dilihat pada Screenshot dari test result pada GUI bahwa Sample Time dari method sebelum di optimize lebih lambat dibandingkan setelah di optimize. Ini menandakan bahwa proses optimisasi yang sudah saya lakukan bisa dibilang berhasil membuat kode saya lebih efisien.
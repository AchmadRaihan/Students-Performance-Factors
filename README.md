# Analyzed Student Performance Factors

### Gambaran Dataset:  
[Student Perfornance Factors](https://www.kaggle.com/datasets/lainguyn123/student-performance-factors) merupakan data yang berisikan tentang faktor yang memengaruhi hasil ujian akhir siswa.

### Background  
Pendidikan merupakan sektor paling penting untuk membangun generasi bangsa yang cerah di masa depan. Namun, dalam beberapa hari terakhir berbagai berita memuat terkait menurunnya kualitas pendidikan di Indonesia. Berdasarkan informasi tersebut, diperoleh data terkait nilai ujian dan faktor yang memengaruhinya. Program ini dibuat untuk memperkirakan nilai ujian akhir yang diperoleh seseorang berdasarkan faktor yang memengaruhinya.
- Berdasarkan data pada nilai ujian, persebaran data sekitar diantara 55 hingga 75 (sangat sedikit orang yang memperoleh nilai diatas 75).
- Bagi mereka yang memperoleh nilai dibawah 70, akan diberikan rekomendasi terkait hal-hal yang harus diperbaiki. Rekomendasi tersebut diberikan berupa parameter/*features*/gaya hidup yang harus diperbaiki dalam menjalani kehidupannya sehingga dapat menjadi bahan evaluasi bagi mereka yang mendapatkan nilai rendah untuk menyadari penyebab gaya hidup yang terbentuk selama ini, apakah sudah cukup bagus untuk dapat mewujudkan ambisi tinggi yang mereka inginkan atau belum. Parameter tersebut diperoleh berdasarkan hasil uji korelasi parameter/*features* terhadap target (pengaruh/korelasi *features* terhadap target)

### Objectives  
- Menganalisis faktor yang memengaruhi siswa terhadap hasil ujian yang diperolehnya.
- Membuat program yang mampu memperkirakan hasil ujian akhir siswa berdasarkan faktor yang memengaruhinya.
- Rekomendasi terhadap siswa yang nilainya dibawah 70.

### Conclusion  
Berdasarkan analisis model yang telah dilakukan, diketahui bahwa **Support Vector Machine** merupakan algoritma terbaik yang dapat digunakan untuk *modeling* melihat pada proses *pipeline* hingga validasi model karena memiliki *mean* yang tinggi namun *standar deviasi* yang rendah. Kemudian, pada *model evaluation* diketahui secara garis besar model masih cenderung *underfit* ketika di evaluasi menggunakan metrik *R2 Score* karena *hyperparameter tuning* yang dilakukan menggunakan *RandomizedSearchCV* dimana hanya mengambil sampel secara acak untuk menetukan parameter terbaik pada model.  
**Kelemahan**  
Penggunaan RandomizedSearchCV dikarenakan kelemahan dari model dari **Support Vector Machine** dimana membutuhkan performa perangkat yang tinggi untuk dapat menjalankan, termasuk *hyperparameter tuning* hingga maksimal. Dengan kelemahan pada perangkat dan beratnya proses *hyperparameter tuning*, maka hanya sedikit parameter yang dapat digunakan demi efisiensi dan efektifitas.  
**Kelebihan**  
**Support Vector Machine** merupakan algoritma dengan performa terbaik yang bukan hanya berdasarkan hasil *model validation*, tetapi juga dapat digunakan untuk analisis data klasifikasi maupun regresi. Adanya *kernel* sangat membantu **Support Vector Machine** sehingga dapat lebih fleksibel untuk berhadapan dengan berbagai jenis pola data yang rumit untuk di *handle*.  
**Improvement**  
Berdasarkan kelemahan pada **Support Vector Machine**, maka terdapat cara untuk mengantisipasi kemungkinan terburuk yang terjadi, yaitu memiliki perangkat yang mumpuni untuk menjalankan model atau *modeling* sedini mungkin sehingga dapat melakukan *hyperparameter tuning* secara maksimal.

Berdasarkan eksplorasi data yang telah dilakukan, terdapat beberapa informasi menarik yang dapat disampaikan, yaitu *Hours Studied* dan *Attendance* merupakan faktor utama yang memengaruhi hasil ujian yang diperoleh tiap siswa berdasarkan uji korelasi menggunakan *phik*. Dengan kedua faktor tersebut menjadi pengaruh yang besar, setelah dilakukan analisis terdapat informasi bahwa jam belajar dan persentase hadir ke kelas yang ideal yaitu sekitar 24 jam/minggu dan 90% kehadiran. Selain itu, jarak tempuh yang dilalui mayoritas siswa dari rumah menuju sekolah cukup dekat. Kemudian, motivasi siswa dalam belajar memengaruhi hasil ujian yang diperoleh. Ini akan menjadi tantangan bagi berbagai pihak agar siswa termotivasi untuk belajar demi mencetak **Generasi Emas Indonesia 2045**. Selanjutnya, peran orang tua penting dalam belajar memengaruhi pembelajaran siswa. Hal itu disebabkan sehebat apapun guru dalam mengajar, orang tua merupakan satu-satunya orang yang paling dekat dan mengenal anaknya sendiri sehingga penting dalam pendidikan.

Berdasarkan informasi diatas, *Hours Studied* dan *Attendance* merupakan faktor yang memengaruhi secara langsung terkait hasil ujian yang diperoleh tiap siswa. Meskipun begitu, terdapat rekomendasi pihak sekolah, orang tua, dan pihak lainnya untuk dapat menunjang dalam memengaruhi siswa sehingga memperoleh hasil ujian yang tinggi, yaitu:
- **Keterlibatan orang tua**: Dalam data yang diperoleh, orang tua memiliki peran penting dalam memengaruhi hasil ujian anaknya. Hal itu hal wajar karena tidak semua orang tua memiliki waktu luang untuk bercengkrama dengan anaknya yang umumnya disebabkan tuntuan pekerjaan atau hal lainnya. Meskipun begitu, orang tua adalah yang paling mengenal anaknya sehingga mereka sangat paham terkait faktor baik buruk perilaku yang dialami anaknya. Maka, sudah sepantasnya orang tua lebih dapat memehartikan dan mengontrol berbagai aktivitas yang dilakukan anak-anaknya.
- **Sumber daya mumpuni**: Faktor ini penting di setiap sekolah karena sangat membantu siswa yang memiliki sarana prasarana yang kurang mendukung dirumahnya dalam pembelajaran, baik itu perpustakaan, akses internet, dan lain-lain.
- **Sesi Tutor bersama teman/orang sepaham**: Faktor ini penting karena tidak semua murid mampu menerima materi yang disampaikan para guru dengan cara mengajar yang dibawakan para guru. Oleh karena itu, biasanya para murid mencari para mentor yang dapat memahami mereka terkait cara menguasai materi pembelajaran, baik itu temannya sendiri, mencari pengajar yang berkarir di luar lingkup sekolahnya, atau melakukan sesi privat dengan guru sewaktu sekolah di luar jam belajar jika guru tersebut berkenan.
- **Sumber daya untuk para disabilitas**: Faktor ini penting karena dapat menunjang para disabilitas dalam pembelajaran di sekolah sehingga mereka memiliki peluang yang sama untuk dapat mencapai hasil ujian yang bagus.

### Justifications  
- [Kriteria Kelulusan Minimal](https://www.quipper.com/id/blog/info-guru/kriteria-ketuntasan-minimal/#Prinsip_penetapan_Kriteria_Ketuntasan_Minimal)  
- [Tanggapan pengamat terkait skor PISA yang menurun](https://news.republika.co.id/berita/sliclh483/skor-pisa-ri-jeblok-semasa-rezim-nadiem-makarim-apa-yang-harus-dibenahi-prof-muti-part3)
- [Berita terkait skor PISA yang menurun](https://www.kompas.id/baca/humaniora/2023/12/10/hasil-pisa-2022-krisis-belajar-yang-belum-juga-menemukan-ujungnya)

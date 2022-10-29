# SIG_Working-with-Projections

*Tutorial Working with Projections

1. Download terlebih dahulu file ne_10m_admin_0_countries.zip dan minisc_gb.zip 

2. Buka QGIS lalu pilih Layer lalu pilih Add Layer lalu pilih Add vektor layer  (*Gambar 1*)

3. Klik ... disebelah Source, Browse file ne_10m_admin_0_countries.shp yang diunduh dan klik Add (*Gambar 2*)

4. Pada bagian bawah jendela QGIS, kita bisa melihat label Coordinate. Saat kita menggerakkan kursor di atas peta, itu akan menunjukkan kepada kita koordinat X dan Y. Di pojok kanan bahwa kita bisa melihat EPSG:4326. Ini adalah kode untuk CRS(Proyeksi) saat ini untuk proyek juga dikenal sebagaiProyek CRS (*Gambar 3*)

5. Untuk menentukan royeksi layer, kita dapat melihat metadata. Klik kanan pada layer ne_10m_admin_0_countries dan pilih properties (*Gambar 4*)

6. Beralih ke tab information dalam dialog Layer Properties. Perluas bagian informasi dari penyedia. Di bagina bawah, kita akan melihat nama proyeksi di bawahCRS (*Gambar 5*)

7. Selanjutnya kita akan melihat bagaimana kita dapat mengubah proyeksi layer. Operasi ini disebut proyeksi ulang. Daripada memproyeksikan ulang seluruh lapisan, kita juga dapat memilih subset fitu dan memproyeksikannya kembali ke layer baru. Gunakan fitur Select Features by area or single click tool dan klik fitur United Kingdom untuk melihatnya (*Gambar 6*)

8. Cari dan temukan algoritma Vector General Reproject layer di Processing toolbar (*Gambar 7*)

9. Pilih ne_10m_admin_0_countries sebagai Input Layer, centang Selected features only lalu klik ikon globe di sebelah target CRS, cari dan pilih EPSG:27700 - OSGB 1936 / British National Grid. Di Reprojected, pilih ...dan klik Save to a file. Sekarang pilih direktori dan masukkan nama sebagai united_kingdom.gkpg dan klik Run (*Gambar 8*)

10. Sebuah layer baru united_kingdom akan muncul di Panel Layer. Seperti yang kita lihat, kedua lapisan masih sejajae satu sama lain meskipun mereka berada di CRS yang berbeda. Ini karena QGIS mendukung transformasi CRS On-The-Fly (OTF). Artinya, setiap kali CRS layer tidak cocok dengan Project CRS, maka secara ditransformasikan ke Project CRS sehingga dapat ditampilkan dengan benar. Sekarang kita atur Project CRS agar sesuai dengan CRS United_Kingdom Layer yang baru dibuat. Hapus layer ne_10m_admin_0_countries dan klik kanan pada layer united_kingdom layer CRS atur Project CRS dari layer (*Gambar 9*)

11. Kita akan melihat Project CRS iperbarui ke EPSG:27700 (*Gambar 10*)

12. Sekarang kita tambahkan layer Raster. Pilih Layer lalu Add layer lalu Add Raster Layer (*Gambar 11*)

13. Klik pada ... di sebelah Source, pilih layer MiniScale_(standard)_R23.tif lalu klik Add (*Gambar 12*)

14. Sekarang layer baru MiniScale_(standard)_R23 ditambahkan ke kanvas (*Gambar 13*)

15. Untuk membuat kedua lapisan terlihat, alihkan urutan lapisan dengan menyeret MiniScale_(standard)_R23 ke bawah di panel layer (*Gambar 14*)

16. Klik kanan pada layer MiniScale_(standard_R23 dan klik Properties (*Gambar 15*)

17. Pada layer Properties, alihkan ke Information, CRS adalah EPSG:27700 - OSBG 1935 / British National Grid - Projected. Ini menegaskan bahwa CRS lapisan raster sam dengan CRS project (*Gambar 16*)

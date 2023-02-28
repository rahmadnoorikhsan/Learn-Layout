# View dan View Group
 semua komponen view dan viewgroup memiliki dua buah atribut penting yang harus selalu diberikan nilai untuk mengatur posisi dirinya di dalam sebuat layout, yaitu:
  - layout_width
  - layout_height
Saya akan menggunakan sebuah obyek ScrollView yang akan menjadi root untuk tampilan halaman aplikasi. 
Saya menggunakan ScrollView sebagai root karena kita ingin halaman aplikasi bisa di-scroll ke bawah dan ke atas. 
Hal ini akan memudahkan pengguna untuk melihat tampilan secara menyeluruh.
ScrollView hanya dapat memiliki satu layout Viewgroup sebagai root untuk obyek View di dalamnya. 
Di sini susunan komponen View akan berorientasi vertikal.
Berikut Arsitektur layout yang saya buat :
  
  <ScrollView>
      <LinearLayout>
          <FrameLayout></FrameLayout>
          <TableLayout>
              <TableRow></TableRow>
          </TableLayout>
          <RelativeLayout></RelativeLayout>
      </LinearLayout>
  </ScrollView>
  
Disini saya menggunakan Style dan Theme untuk mempermudah dalam mengatur Layout. Berikut penjelasan singkat Style dan Theme :
==
Style
--
Style merupakan sebuah kumpulan properti yang dibutuhkan untuk mendefinisikan bagaimana sebuah komponen view dan layar jendela (bisa activity maupun fragment) ditampilkan. Contoh properti ini adalah height, width, background_color.
Pemusatan style cocok digunakan untuk mengumpulkan attribute yang berulang-ulang digunakan di banyak komponen. Sehingga jika ada perubahan, Anda cukup mengubahnya di satu tempat saja. Style terdefinisi dalam file xml sendiri. Anda bisa menemukannya di res → values → themes.xml.
==
Theme
--
Theme atau tema itu sendiri merupakan sebuah style yang diterapkan khusus untuk activity dan application pada berkas AndroidManifest.xml.kita mendefinisikannya dengan cara berikut ini:

android:theme="@style/Theme.NamaProject"

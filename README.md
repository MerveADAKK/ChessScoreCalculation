# Chess Score Calculation
Problem tanımı: Satranç tahtası üzerinde bulunan taşlara göre iki tarafın (siyah – beyaz) mevcut durumlarının puan hesaplaması.

Açıklama: Mevcut puanı hesaplama algoritması şöyledir:

1. Bir taşın tehdit altında olup olmadığının kontrolü, o taşı tehdit eden karşı renkte bir veya birden fazla taş olması durumunda oluşur.

2. Tablo 1 ’de taşların puanları verilmiştir. Eğer bir taş tehdit edilmiyorsa tablodaki puanı alır.

3. Eğer bir taş karşı tarafın taşlarından herhangi biri tarafından tehdit ediliyorsa, tehdit edilen taşın puanı Tablo 1’deki puanının yarısı alınır.

4. Tüm taşların tehdit durumları kontrol edilir. Siyah ve beyaz taşlar için iki ayrı puan hesaplanır.


<i>Tablo 1 Satranç Taşları ve Puanları</i>
<table><tbody><tr><th>Taş İsmi</th><th>Kısaltma</th><th>Puanı</th></tr><tr><td>Piyon</td><td>p</td><td>1</td></tr><tr><td>At</td><td>a</td><td>3</td></tr><tr><td>Fil</td><td>f</td><td>3</td></tr><tr><td>Kale</td><td>k</td><td>5</td></tr><tr><td>Vezir</td><td>v</td><td>9</td></tr><tr><td>Şah</td><td>s</td><td>100</td></tr></tbody></table>


<p>Örnek:</p>

<img src="https://r.resimlink.com/1q6CJd.png" alt="Chess" width="400" height="400">
<p> Puan hesabı, tehdit altında olan taşlara göre şöyle hesaplanabilir: </p>
<p> Siyah = (3*0.5)+(5*1)+(3*2)+(3*2)+(5*2)+9+100 = 137.5</p>
<p> Beyaz = (1*0.5)+(7*1)+(3*2)+(3*2)+(5*2)+9+100 = 138.5</p>

<h2> Çözüm </h2>

<p> Kod Java programlama dili ile Intellij Idea ortamında hazırlanmıştır. </p> 
<p> Projede 9 tane class yer almaktadır. </p>
<img src="https://r.resimlink.com/ws68CeP.png" alt="Class">
<p> Piece abstract classtır. Bu sınıftan kalıtım alan sınıflar ise: Bishop(Fil), King(Şah), Knight(At), Pawn(Piyon), Queen(Vezir), Rook(Kale)
 
<p>Test için 3 tane dosya ve olması gereken sonuçlar eklenmiştir. </p>
<p> Yaptığım test sonucunda aşağıda ki sonuçlar çıkmıştır: <br>
  board1.txt -> Siyah:133.5 Beyaz:134.5 <br>
  board2.txt -> Siyah:116.0 Beyaz:123.0 <br>
  board3.txt -> Siyah:108.0 Beyaz:109.0 </p>
  
  
  <h2> Kurulum </h2>
  <p> Program Java dili ile yazılmıştır. Java kodu çalıştırabilen herhangi geliştirme ortamında çalıştırabilirsiniz. Ben Intellij Idea kullandım. </p>
  <p> <img src="https://r.resimlink.com/rQV50.png" alt="CsTechChess.zip"> Yukarıda bu isimde ki dosyadan kodu bilgisayarınıza indirebilirsiniz. </p>
  <p> Kodumuzu yüklediğimizde dosyalar bu şekilde gözükecektir. </p>
  
  <img src="https://r.resimlink.com/q3tmOg_07voL.png" alt="Code screen">
  
  <p> Main classımızdan kodumuzu çalıştırdığımızda istediğimiz sonucu almaktayız. Main classında 7. satırda kontrol etmesini istediğimiz txt dosyasının ismini değiştirebilmekteyiz. </p>
  
    
  <img src="https://r.resimlink.com/Q5u4IfMoF.png" alt="Code screen2">
  
 



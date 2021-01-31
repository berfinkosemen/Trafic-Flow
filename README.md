# Trafic-Flow

Trafik Akışının Modellenmesi

Berfin Kösemen	  
Fatma Değirmenci  

Bu README.md dosyası, Trafik Akışının Modellenmesi projesine aittir.
Bu paket, kaynak kodu ile aynı dizin içerisinde bulunacaktır.


1-PAKETİN İÇERİĞİ:
-------------------
170201008-170201058.c - Projenin tek dosyaya indirgenmiş salt kaynak kodu.
README.md - Bu dosya.
-------------------


2-SİSTEM GEREKSİNİMLERİ:
-------------------
gcc - GNU Compiler Colection - http://gcc.gnu.org/
-------------------


3-KURULUM:
-------------------
Paket içeriğini yukarıda görebilirsiniz.

Bu kod, iki adet Windows kurulu makinede çalıştırıldı:
- Fatma'nın Windows 10 yüklü dizüstü bilgisayarında.
- Berfin'in Windows 10 yüklü masaüstü bilgisayarında.

Bu iki durumda da kod, herhangi bir hata vermeden, daha önceden belirlenen kriterlere
uygun çalıştı.

Windows harici bir makinede çalıştırmak istiyorsanız, kaynak kodu Windows
bağımlılıklarından ayırıp derlemeniz gerekiyor.

-------------------


4-KODU DERLEMEK:
------------------
Artık bilgisayarımızda kurulu olan GCC ile kodu kolayca derleyebiliriz.

Windows için:

>gcc 170201008-170201058.cpp –o TrafikAkisininModellenmesi.exe

Linux / Unix için:

>gcc 170201008-170201008.cpp -o Labirent


Derleme bittikten sonra kolayca programı çalıştırabilirsiniz.
------------------


5- PARAMETRELER
---------------------------
Kodun çalışması için başlangıçta herhangi bir parametre gerekmiyor.
------------------


6- PROGRAMIN KULLANIMI
-----------------------------
Trafik Akışının Modellenmesi, kullanıcıdan, her yol için yön bilgisi
ve ortalama araç sayısı alarak, bilinmeyen yolların ortalama araç
sayısının Gauss-Jordan ile bulunup, ekrana yazdırılmasını sağlar.

Ekrana 2 harita da yazdırılır ve kullanıcıdan seçim yapması istenilir.
Yalnızca 1 ya da 2 seçimini yapabilir.

Harita seçiminin ardından, seçilen giriş ve çıkış yollarında, en 
fazla 2 giriş ve 2 çıkış seçilebilir.

Seçilen haritaya göre kullanıcıdan her yolun yön ve başlangıç noktası
bilgisi alınır. Düğümlerde çakışma olması halinde bir yolun yönünün
değiştirilmesi istenilir. 

Seçilen yönler hareketli bir şekilde ekranda gösterilir. Bu ekrandan
çıkmak için bir tuşa basılmalıdır.

Her yol için, kullanıcıdan ortalama araç sayısı bilgisi alınır. Bilinmeyen
yollar için -1 değeri girilmelidir. Tüm yolların ortalama araç sayısı 
girişi bittiğinde eğer 1'den az ya da 5'ten çok bilinmeyen yol girişi
yapılmış ise, program bilinmeyen yolların araç yoğunluğunu hesaplayamaz.

Verilen yön bilgisi ve ortalama araç sayıları kapsamında, denklemlere göre
katsayıları bir matrise atama işlemi gerçekleştikten sonra denklem sistemi
çözülürken yapılan her adım ekranda kullanıcıya gösterilecektir.

Denklem sistemi çözüldükten sonra çözümünün olup olmadığı ekrana yazdırılacak
ve programdan çıkılacaktır.

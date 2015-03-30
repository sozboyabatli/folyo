#   Git

.fx: first

Simge Özboyabatlı `<simge.ozboyabatli@bil.omu.edu.tr>`

İsmail Arslan  `<ismail.arslan@bil.omu.edu.tr>`

Mart 2015

![alt text](/home/sozboyabatli/folyo/git/media/Git.png "Logo")

##  Git Nedir?

-   Bir versiyon kontrol sistemi

-   Projelerde çalışma kolaylığı

-   Dağıtık bir yapı

![alt text](/home/sozboyabatli/folyo/git/media/at.jpg "Oğlumbakgit")

##  Git Tarihçesi (Lisans & Neden Üretildi)

-   Yıl 2005 Linus Torvalds 

-   Şimdilerde Junio Hamano

-   İlk olarak Linux çekirdeğinin kaynak kodlarına gerekliydi

-   Performans yüksek olmalıydı

-   Belli bir merkezle sınırlı olmamalıydı

-   Veri kaybına izin verilmemeliydi

-   GNU Genel Kamu Lisansı v2

##  Zorunda mıyım?

-   Mercurial (2005)

-   SVN (Subversion) (2000)

-   Bazaar (2005)

-   Fossil (2006)

-   CVS (Concurrent Version System) (1990)

-   Ve daha niceleri...

##  Peki Neden Git Anlatsana Biraz...

-   Aynı anda birden fazla çalışma merkezi

-   Çok hızlı

-   Kolay iş bölümlemesi

-   Lineer olmayan iş akışı (Branching)

-   Tamamen dağıtık

-   Büyük projeleri detekleyebilecek

-   Çevrimdışı çalışma imkanı

##  Dezavantajları

![alt text](/home/sozboyabatli/folyo/git/media/yokki.jpg "Yokki")

##  Kurulum

	!sh
	$ sudo apt-get install git

##  Sıfırdan Depo Oluşturma 

	!sh
	$ cd proje/dizini/
	$ git init

##  Dosyaları Depoya Ekleme

	!sh
	$ git add dosya_adi   // değişiklik yapılan dosyayı ekleme

	$ git add -A         //	git takibindeki herşeyi depoya ekleme

##  Uzak Depo Oluşturma

	!sh
	$ git remote add origin <sunucu>

##  Hangi Erişim Şekli

-   git://bişeyler.bişeyler

-   ssh://bişeyler.bişeyler

-   https://bişeyler.bişeyler

[Hangi Protokol Kullanılmalı?](https://help.github.com/articles/which-remote-url-should-i-use/)

##  Depo Klonlama

	!sh
	$ git clone depo_adresi

##  Değişiklikleri Kaydetmek İstersem

	!sh
	$ git commit -m "Değişiklik"

##  Uzaktaki Depoya Göndermek İçin

	!sh
	$ git push origin master

## Uzak Depodaki Değişiklikler

	!sh
	$ git pull   // fetch+merge aslında

##  Dal Oluşturma

	!sh
	$ git branch dal_adı

##  Dal Silme

	!sh
	$ git branch -d dal_adı

##  Başka Dala Geçme

	!sh
	$ git checkout dal_adı

##  Değişiklikleri Birleştirmek İçin

	!sh
	$ git merge dal_adı

##  İstenmeyen Dosyalar

	!sh
	$ touch .gitignore

##  Hmm... Peki Yapılandırma?

-   Birinci seviye → /etc/git/config

        !sh
        $ git config --system

-   İkinci seviye → /.gitconfig

        !sh
        $ git config global

-   Üçüncü seviye → /projedizini/.git/config
	
        !sh
        $ vim config

##  Uzak Depoyu Değiştirme

[Uzak depo URL değiştirme & Protokoller arası geçiş](https://help.github.com/articles/changing-a-remote-s-url/)

##  Son Commit Bilgilerini Düzenleme

-   Son commit işlemini düzeltmemize yarar

        !sh
        $ git commit --amend   

##  Local Değişiklikleri Geri Alma 

-   Henüz commit etmediğiniz durumda dosya değişikliği için
	
        !sh
        $ git checkout -- dosya_ad

-   Tüm dosyalardaki değişiklikleri geri almak için 

        !sh
        $ git reset --hard HEAD

##  Commit Edilmiş Bir Değişikliği Geri Almak 

-   Commit işlemindeki değişiklikler geri alınır, eski commit ve işlemler silinmez
	
        !sh
        $ git revert commit_hash

-   Değişiklikleri geri alır, revert işleminden farkı yeni commit oluşturmaz

-   Reset ile kullanılan --hard değişiklikleri siler --keep değişiklikleri korur

        !sh
        $ git reset --hard commit_hash

##  İki Versiyon arasındaki Farklar

        !sh
        $ git diff
        $ git diff a..b   // commitlerin hash değerleri yazılıp karşılaştırılması

##  Local Branch Üzerindeki Değişimler

	!sh
	$ git status

##  Commit Edilmiş Dosya Değişiklikleri

	!sh
	$ git log   // -p içerik değişiklikleri

#   Teşekkürler

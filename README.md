<p align="center">
<img src="source/header.png" alt="Header Image">
</p>
<h3 align="center">Github Öğrenme Yolculuğu İçin Başvuru Dokümanı</h3>
<p align="center">
    <span><a href="https://github.com/btr316530/github-learning/issues/new?assignees=&labels=bug&template=bug_report.md&title">Hata Bildir</a></span>
    <span><a href="https://github.com/btr316530/github-learning/issues/new?assignees=&labels=feature&template=feature_request.md&title">Özellik İste</a></span>
</p>

# GitHub Nedir?

GitHub, yazılım geliştirme projeleri için web tabanlı bir versiyon kontrol ve işbirliği platformudur. Git versiyon kontrol sistemini kullanarak projelerinizi yönetmenizi sağlar. GitHub, kod depolarınızı barındırmanıza, değişiklikleri takip etmenize ve diğer geliştiricilerle işbirliği yapmanıza olanak tanır.

## İçindekiler

- [GitHub Nedir?](#github-nedir)
- [Temel Özellikler](#temel-özellikler)
- [Commit Mesajları Nasıl Olmalı?](#commit-mesajları-nasıl-olmalı)
  - [Örnek Commit Mesajları](#örnek-commit-mesajları)
- [Kullanıcı Bilgilerini Ayarlama](#kullanıcı-bilgilerini-ayarlama)
- [Git Clone Kullanımı](#git-clone-kullanımı)
  - [Depoyu Klonlama](#depoyu-klonlama)
  - [Belirli Bir Dizin Adıyla Klonlama](#belirli-bir-dizin-adıyla-klonlama)
- [Git Branch Kullanımı](#git-branch-kullanımı)
  - [Yeni Bir Dal Oluşturma](#yeni-bir-dal-oluşturma)
  - [Dalları Listeleme](#dalları-listeleme)
  - [Bir Dala Geçiş Yapma](#bir-dala-geçiş-yapma)
  - [Yeni Bir Dal Oluşturma ve Geçiş Yapma](#yeni-bir-dal-oluşturma-ve-geçiş-yapma)
  - [Dal Silme](#dal-silme)
- [Git Remote Kullanımı](#git-remote-kullanımı)
  - [Uzak Depo Ekleme](#uzak-depo-ekleme)
  - [Uzak Depoları Listeleme](#uzak-depoları-listeleme)
  - [Uzak Depodan Değişiklikleri Çekme](#uzak-depodan-değişiklikleri-çekme)
  - [Uzak Depodan Değişiklikleri Çekme ve Birleştirme](#uzak-depodan-değişiklikleri-çekme-ve-birleştirme)
  - [Uzak Depoya Değişiklikleri Gönderme](#uzak-depoya-değişiklikleri-gönderme)
  - [Uzak Depoyu Kaldırma](#uzak-depoyu-kaldırma)
- [Git Merge Kullanımı](#git-merge-kullanımı)
  - [Dalları Birleştirme](#dalları-birleştirme)
  - [Birleştirme Çatışmalarını Çözme](#birleştirme-çatışmalarını-çözme)
- [Git Log Kullanımı](#git-log-kullanımı)
- [Commit İşlemleri](#commit-işlemleri)
  - [Değişiklikleri Commit Etme](#değişiklikleri-commit-etme)
  - [Commit Mesajı Düzenleme](#commit-mesajı-düzenleme)
  - [Değişiklikleri Geri Alma](#değişiklikleri-geri-alma)
  - [Commit Geçmişini İnceleme](#commit-geçmişini-inceleme)
- [Commit Silme](#commit-silme)
  - [Son Commit'i Silme](#son-commiti-silme)
  - [Belirli Bir Commit'i Silme](#belirli-bir-commiti-silme)
  - [Commit'i Geri Alma](#commiti-geri-alma)

## Temel Özellikler

- **Depolar (Repositories):** Projelerinizi barındırdığınız yerlerdir.
- **Dallanma (Branching):** Farklı özellikler veya düzeltmeler üzerinde çalışmak için dallar oluşturabilirsiniz.
- **Çekme İstekleri (Pull Requests):** Değişikliklerinizi ana projeye entegre etmek için isteklerde bulunabilirsiniz.
- **Sorunlar (Issues):** Projenizle ilgili hataları veya iyileştirme önerilerini takip edebilirsiniz.
- **Wiki:** Projenizle ilgili belgeleri oluşturup paylaşabilirsiniz.

GitHub, açık kaynak projelerden özel projelere kadar geniş bir yelpazede kullanılabilir ve geliştiricilere güçlü bir işbirliği ortamı sunar.

## Commit Mesajları Nasıl Olmalı?

İyi bir commit mesajı, yapılan değişikliklerin amacını ve kapsamını açıkça belirtmelidir. Aşağıda, etkili commit mesajları yazmak için bazı ipuçları bulunmaktadır:

1. **Kısa ve Öz Olun:** Başlık kısmı 50 karakteri geçmemelidir. Gerekiyorsa daha detaylı açıklamaları alt satırlarda verebilirsiniz.
2. **Emir Kipinde Yazın:** "Eklendi", "Düzeltildi" gibi geçmiş zaman kullanmak yerine "Ekle", "Düzelt" gibi emir kipinde yazın.
3. **Neden ve Ne Sorularını Cevaplayın:** Yapılan değişikliğin neden yapıldığını ve neyi değiştirdiğini açıklayın.
4. **Bağlam Sağlayın:** Değişikliklerin hangi sorunu çözdüğünü veya hangi özelliği eklediğini belirtin.
5. **Numaralandırma ve Referanslar:** İlgili ise, sorun numaralarını veya referansları ekleyin.

### Örnek Commit Mesajları

```console
feat: kullanıcı giriş sistemi eklendi
```

Kullanıcıların sisteme giriş yapabilmesi için gerekli olan kimlik doğrulama mekanizması eklendi. Bu değişiklik, kullanıcıların kişisel hesaplarına erişimini sağlar.

```console
fix: ana sayfadaki yazım hatası düzeltildi
```

Ana sayfadaki "Hoşgeldiniz" başlığındaki yazım hatası düzeltildi. Bu değişiklik, kullanıcı deneyimini iyileştirir.

```console
docs: README dosyasında değişiklik yapıldı.
```

README gibi dokümanlarda değişiklik yapıldığını bildirmek için uygundur.

```console
perf: Kod performası arttırıldı.
```

Performansı etkileyen değişiklikleri bildirmek için kullanıma uygun.

İyi yazılmış commit mesajları, proje geçmişini anlamayı kolaylaştırır ve ekip içi iletişimi geliştirir.

## Kullanıcı Bilgilerini Ayarlama

Git yapılandırma ayarlarını global düzeyde ayarlamak için kullanılır. Global düzeyde yapılan ayarlar, bilgisayarınızdaki tüm Git depoları için geçerli olur.

```console
git config --global user.name <username>
git config --global user.email <useremail>
```

Bu komutlar, Git kullanıcı adınızı ve e-posta adresinizi ayarlar. Bu bilgiler, Git ile yaptığınız tüm işlemlerde kullanılacaktır.

```console
git config --global user.name "yucel-yilmaz"
git config --global user.email "yucelyilmaz.en@gmail.com"
```

Bu ayarlar, Git commit'lerinde kimlik bilgilerinizi belirlemek için kullanılır. Böylece, commit'lerinizin kim tarafından yapıldığını izlemek mümkün olur.

## Git Clone Kullanımı

Git clone komutu, uzak bir depoyu yerel bilgisayarınıza kopyalamak için kullanılır. Bu komut, projeyi baştan sona indirir ve yerel bir Git deposu oluşturur.

### Depoyu Klonlama

Bir projeyi klonlamak için aşağıdaki komutu kullanabilirsiniz:

```console
git clone <repository-url>
```

Bu komut, belirtilen URL'deki depoyu yerel bilgisayarınıza indirir. Depo, URL'den alınan ada sahip bir dizin olarak oluşturulur.

### Belirli Bir Dizin Adıyla Klonlama

Depoyu belirli bir dizin adıyla klonlamak için:

```console
git clone <repository-url> <directory-name>
```

Bu komut, depoyu belirtilen dizin adıyla indirir.

Git clone komutu, projeye hızlı bir başlangıç yapmak ve mevcut bir projeyi yerel ortamınıza getirmek için kullanışlıdır.

## Git Branch Kullanımı

Git branch komutu, dalları yönetmek için kullanılır. Dallar, projede paralel çalışmalar yapmayı ve farklı özellikler üzerinde çalışmayı kolaylaştırır.

### Yeni Bir Dal Oluşturma

Yeni bir dal oluşturmak için:

```console
git branch <branch-name>
```

Bu komut, mevcut dalın bir kopyasını oluşturur ve yeni bir dal oluşturur.

### Dalları Listeleme

Mevcut dalları listelemek için:

```console
git branch
```

Bu komut, yerel depodaki tüm dalları listeler ve şu anda hangi dalda olduğunuzu gösterir.

### Bir Dala Geçiş Yapma

Başka bir dala geçiş yapmak için:

```console
git checkout <branch-name>
```

Bu komut, belirtilen dala geçiş yapar ve çalışma dizininizi o dalın son commit'ine göre günceller.

### Yeni Bir Dal Oluşturma ve Geçiş Yapma

Yeni bir dal oluşturup aynı anda o dala geçiş yapmak için:

```console
git switch -c <branch-name>
```

Bu komut, yeni bir dal oluşturur ve otomatik olarak o dala geçiş yapar.

### Dal Silme

Bir dalı silmek için:

```console
git branch -d <branch-name>
```

Bu komut, belirtilen dalı siler. Eğer dalda henüz birleştirilmemiş değişiklikler varsa, -D seçeneğini kullanarak zorla silebilirsiniz:

```console
git branch -D <branch-name>
```

Git branch komutu, projede dallar oluşturmak, yönetmek ve dallar arasında geçiş yapmak için kullanışlıdır.

## Git Remote Kullanımı

Git remote komutları, yerel Git deposunu uzak bir depoya bağlamak ve yönetmek için kullanılır. Uzak depolar, projelerinizi GitHub gibi platformlarda barındırmanızı sağlar.

### Uzak Depo Ekleme

Bir projeye uzak depo eklemek için aşağıdaki komutu kullanabilirsiniz:

```console
git remote add origin <repository-url>
```

Bu komut, yerel deponuzu belirtilen URL'deki uzak depoya bağlar. "origin" genellikle varsayılan uzak depo adı olarak kullanılır.

### Uzak Depoları Listeleme

Bağlı olduğunuz uzak depoları listelemek için:

```console
git remote -v
```

Bu komut, uzak depo adlarını ve URL'lerini gösterir.

### Uzak Depodan Değişiklikleri Çekme

Uzak depodan en son değişiklikleri almak için:

```console
git fetch origin
```

Bu komut, uzak depodaki değişiklikleri yerel deponuza getirir ancak çalışma dizininize uygulamaz.

### Uzak Depodan Değişiklikleri Çekme ve Birleştirme

Uzak depodaki değişiklikleri yerel deponuza çekmek ve otomatik olarak birleştirmek için:

```console
git pull origin main
```

Bu komut, "origin" uzak deposundaki "main" dalındaki değişiklikleri yerel "main" dalınıza çeker ve birleştirir. Eğer birleştirme sırasında çatışmalar oluşursa, bu çatışmaları çözmeniz gerekecektir.

### Uzak Depoya Değişiklikleri Gönderme

Yerel deponuzdaki değişiklikleri uzak depoya göndermek için:

```console
git push origin main
```

Bu komut, yerel "main" dalındaki değişiklikleri "origin" uzak deposuna gönderir.

### Uzak Depoyu Kaldırma

Bir uzak depoyu kaldırmak için:

```console
git remote remove origin
```

Bu komut, "origin" adlı uzak depoyu yerel deponuzdan kaldırır.

Git remote komutları, projelerinizi uzak depolarla senkronize etmek ve işbirliği yapmak için önemlidir.

## Git Merge Kullanımı

Git merge komutu, farklı dallardaki değişiklikleri birleştirmek için kullanılır. Bu komut, bir dalın içeriğini başka bir dala entegre eder.

### Dalları Birleştirme

Bir dalı başka bir dala birleştirmek için önce hedef dalı checkout yapın:

```console
git checkout main
```

Ardından, birleştirmek istediğiniz dalı belirtin:

```console
git merge feature-branch
```

Bu komut, "feature-branch" dalındaki değişiklikleri "main" dalına birleştirir.

### Birleştirme Çatışmalarını Çözme

Birleştirme sırasında çatışmalar oluşabilir. Çatışmaları çözmek için ilgili dosyaları düzenleyin ve değişiklikleri commit yapın:

```console
git add <conflicted-files>
git commit
```

Birleştirme işlemi tamamlandığında, değişiklikler hedef dalda birleştirilmiş olur.

Git merge komutu, farklı dallardaki çalışmaları entegre etmek ve projeyi birleştirmek için kullanışlıdır.

## Git Log Kullanımı

Git projenizdeki commit geçmişini görüntülemek için aşağıdaki komutu kullanabilirsiniz:

```console
git log
```

Bu komut, projenizdeki tüm commit'lerin bir listesini gösterir. Her commit için yazar, tarih ve commit mesajı gibi bilgiler görüntülenir.

Commit geçmişini daha okunabilir hale getirmek için çeşitli seçenekler kullanabilirsiniz:

```console
git log --oneline
```

Bu komut, her commit'i tek bir satırda özetler. Commit hash'i ve commit mesajının ilk satırı gösterilir.

```console
git log --graph --decorate --oneline
```

Bu komut, commit geçmişini grafiksel olarak gösterir ve dallanmaları görselleştirir. Ayrıca, commit'lere eklenen etiketler ve dallar gibi süslemeler de gösterilir.

```console
git log --author="yucel-yilmaz"
```

Bu komut, belirli bir yazar tarafından yapılan commit'leri filtreler. Yazar adı yerine e-posta adresi de kullanılabilir.

```console
git log --since="2023-01-01" --until="2023-12-31"
```

Bu komut, belirli bir tarih aralığındaki commit'leri filtreler. Tarihler yerine "2 weeks ago" gibi relative zaman ifadeleri de kullanılabilir.

Git log komutları, projenizin geçmişini anlamak ve belirli değişiklikleri takip etmek için güçlü araçlardır.

## Commit İşlemleri

Git commit komutu, yapılan değişiklikleri kaydetmek için kullanılır. Commit işlemi, projenizdeki değişiklikleri bir noktada dondurur ve bu değişikliklerin kaydını tutar.

### Değişiklikleri Commit Etme

Değişiklikleri commit etmek için önce değişiklikleri sahneleyin:

```console
git add <file>
```

Tüm değişiklikleri sahnelemek için:

```console
git add .
```

Ardından, değişiklikleri commit edin:

```console
git commit -m "Commit mesajı"
```

Bu komut, sahnelenmiş değişiklikleri kaydeder ve belirtilen mesajı commit mesajı olarak kullanır.

### Commit Mesajı Düzenleme

Eğer commit mesajını düzenlemek isterseniz:

```console
git commit --amend
```

Bu komut, son commit mesajını düzenlemenizi sağlar. Ayrıca, son commit'e ek değişiklikler de ekleyebilirsiniz.

### Değişiklikleri Geri Alma

Eğer commit işlemini geri almak isterseniz:

```console
git revert <commit-hash>
```

Bu komut, belirtilen commit'i geri alır ve yeni bir commit oluşturur. Commit hash'i, geri almak istediğiniz commit'in hash değeridir.

### Commit Geçmişini İnceleme

Commit geçmişini incelemek için:

```console
git log
```

Bu komut, projenizdeki tüm commit'lerin bir listesini gösterir. Daha okunabilir bir format için:

```console
git log --oneline
```

Commit işlemleri, projenizdeki değişiklikleri kaydetmek ve takip etmek için temel bir Git işlevselliğidir.

## Commit Silme

Git'te commit silme işlemi dikkatli yapılması gereken bir işlemdir. Commit'leri silmek, proje geçmişini değiştirebilir ve diğer işbirlikçilerle uyumsuzluklara yol açabilir. Commit'leri silmek için iki yaygın yöntem vardır: `git reset` ve `git revert`.

### Son Commit'i Silme

Son commit'i silmek için:

```console
git reset --hard HEAD~1
```

Bu komut, son commit'i ve yapılan değişiklikleri tamamen siler. Eğer değişiklikleri korumak isterseniz, `--soft` seçeneğini kullanabilirsiniz:

```console
git reset --soft HEAD~1
```

Bu komut, son commit'i siler ancak değişiklikleri korur ve sahnelenmiş olarak bırakır.

### Belirli Bir Commit'i Silme

Belirli bir commit'i silmek için:

```console
git rebase -i <commit-hash>^
```

Bu komut, belirtilen commit'in öncesindeki commit'i interaktif rebase modunda açar. Açılan editörde, silmek istediğiniz commit'in satırını `pick` yerine `drop` olarak değiştirin ve dosyayı kaydedin.

### Commit'i Geri Alma

Commit'i tamamen silmek yerine geri almak için:

```console
git revert <commit-hash>
```

Bu komut, belirtilen commit'in etkilerini geri alır ve yeni bir commit oluşturur. Bu yöntem, proje geçmişini koruyarak değişiklikleri geri almak için daha güvenlidir.

Commit silme işlemleri, proje geçmişini düzenlemek ve istenmeyen değişiklikleri geri almak için kullanışlıdır. Ancak, bu işlemleri yaparken dikkatli olunmalı ve mümkünse diğer işbirlikçilerle iletişim kurulmalıdır.

## Destek Olun

Bu projeye destek olmak için aşağıdaki bağlantıları kullanabilirsiniz:

- [Bağış Yap](https://github.com/btr316530/github-learning/issues/new?assignees=&labels=feature&template=feature_request.md&title)
- [Katkıda Bulun](https://github.com/btr316530/github-learning/issues/new?assignees=&labels=bug&template=bug_report.md&title)

## Destekleyenler

Tüm destekleyenlere teşekkürler!

- [Katkıda Bulunanlar](https://github.com/btr316530/github-learning/graphs/contributors)

## Lisans

Bu proje MIT Lisansı ile lisanslanmıştır. Daha fazla bilgi için [LICENSE](LICENSE) dosyasına bakabilirsiniz.

[def]: ttps://github.com/btr316530/github-learning/issues/new?assignees=&labels=feature&template=feature_request.md&title
[def2]: ttps://github.com/btr316530/github-learning/issue
[def3]: def

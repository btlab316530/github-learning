# GitHub Nedir?

GitHub, yazılım geliştirme projeleri için web tabanlı bir versiyon kontrol ve işbirliği platformudur. Git versiyon kontrol sistemini kullanarak projelerinizi yönetmenizi sağlar. GitHub, kod depolarınızı barındırmanıza, değişiklikleri takip etmenize ve diğer geliştiricilerle işbirliği yapmanıza olanak tanır.

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

### Kullanıcı Bilgilerini Ayarlama

```console
git config --global user.name <username>
git config --global user.email <useremail>
```

Git yapılandırma ayarlarını global düzeyde ayarlamak için kullanılır. Global düzeyde yapılan ayarlar, bilgisayarınızdaki tüm Git depoları için geçerli olur.

```console
git config --global user.name "yucel-yilmaz"
```

Bu komut, Git kullanıcı adınızı ayarlar. Bu kullanıcı adı, Git ile yaptığınız tüm işlemlerde kullanılacaktır.

```console
git config --global user.email "yucelyilmaz.en@gmail.com":
```

Bu komut, Git kullanıcı e-posta adresinizi ayarlar. Bu e-posta adresi, Git ile yaptığınız tüm işlemlerde kullanılacaktır.
Bu ayarlar, Git commit'lerinde kimlik bilgilerinizi belirlemek için kullanılır. Böylece, commit'lerinizin kim tarafından yapıldığını izlemek mümkün olur.

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

### Git Clone Kullanımı

Git clone komutu, uzak bir depoyu yerel bilgisayarınıza kopyalamak için kullanılır. Bu komut, projeyi baştan sona indirir ve yerel bir Git deposu oluşturur.

#### Depoyu Klonlama

Bir projeyi klonlamak için aşağıdaki komutu kullanabilirsiniz:

```console
git clone <repository-url>
```

Bu komut, belirtilen URL'deki depoyu yerel bilgisayarınıza indirir. Depo, URL'den alınan ada sahip bir dizin olarak oluşturulur.

#### Belirli Bir Dizin Adıyla Klonlama

Depoyu belirli bir dizin adıyla klonlamak için:

```console
git clone <repository-url> <directory-name>
```

Bu komut, depoyu belirtilen dizin adıyla indirir.

Git clone komutu, projeye hızlı bir başlangıç yapmak ve mevcut bir projeyi yerel ortamınıza getirmek için kullanışlıdır.

### Git Branch Kullanımı

Git branch komutu, dalları yönetmek için kullanılır. Dallar, projede paralel çalışmalar yapmayı ve farklı özellikler üzerinde çalışmayı kolaylaştırır.

#### Yeni Bir Dal Oluşturma

Yeni bir dal oluşturmak için:

```console
git branch <branch-name>
```

Bu komut, mevcut dalın bir kopyasını oluşturur ve yeni bir dal oluşturur.

#### Dalları Listeleme

Mevcut dalları listelemek için:

```console
git branch
```

Bu komut, yerel depodaki tüm dalları listeler ve şu anda hangi dalda olduğunuzu gösterir.

#### Bir Dala Geçiş Yapma

Başka bir dala geçiş yapmak için:

```console
git checkout <branch-name>
```

Bu komut, belirtilen dala geçiş yapar ve çalışma dizininizi o dalın son commit'ine göre günceller.

#### Yeni Bir Dal Oluşturma ve Geçiş Yapma

Yeni bir dal oluşturup aynı anda o dala geçiş yapmak için:

```console
git switch -c <branch-name>
```

Bu komut, yeni bir dal oluşturur ve otomatik olarak o dala geçiş yapar.

#### Dal Silme

Bir dalı silmek için:

```console
git branch -d <branch-name>
```

Bu komut, belirtilen dalı siler. Eğer dalda henüz birleştirilmemiş değişiklikler varsa, -D seçeneğini kullanarak zorla silebilirsiniz:

```console
git branch -D <branch-name>
```

Git branch komutu, projede dallar oluşturmak, yönetmek ve dallar arasında geçiş yapmak için kullanışlıdır.

### Git Remote Kullanımı

Git remote komutları, yerel Git deposunu uzak bir depoya bağlamak ve yönetmek için kullanılır. Uzak depolar, projelerinizi GitHub gibi platformlarda barındırmanızı sağlar.

#### Uzak Depo Ekleme

Bir projeye uzak depo eklemek için aşağıdaki komutu kullanabilirsiniz:

```console
git remote add origin <repository-url>
```

Bu komut, yerel deponuzu belirtilen URL'deki uzak depoya bağlar. "origin" genellikle varsayılan uzak depo adı olarak kullanılır.

#### Uzak Depoları Listeleme

Bağlı olduğunuz uzak depoları listelemek için:

```console
git remote -v
```

Bu komut, uzak depo adlarını ve URL'lerini gösterir.

#### Uzak Depodan Değişiklikleri Çekme

Uzak depodan en son değişiklikleri almak için:

```console
git fetch origin
```

Bu komut, uzak depodaki değişiklikleri yerel deponuza getirir ancak çalışma dizininize uygulamaz.

#### Uzak Depodan Değişiklikleri Çekme ve Birleştirme

Uzak depodaki değişiklikleri yerel deponuza çekmek ve otomatik olarak birleştirmek için:

```console
git pull origin main
```

Bu komut, "origin" uzak deposundaki "main" dalındaki değişiklikleri yerel "main" dalınıza çeker ve birleştirir. Eğer birleştirme sırasında çatışmalar oluşursa, bu çatışmaları çözmeniz gerekecektir.

Git pull komutu, uzak depodaki en son değişiklikleri yerel deponuza entegre etmek için kullanışlıdır.

### Git Merge Kullanımı

Git merge komutu, farklı dallardaki değişiklikleri birleştirmek için kullanılır. Bu komut, bir dalın içeriğini başka bir dala entegre eder.

#### Dalları Birleştirme

Bir dalı başka bir dala birleştirmek için önce hedef dalı checkout yapın:

```console
git checkout main
```

Ardından, birleştirmek istediğiniz dalı belirtin:

```console
git merge feature-branch
```

Bu komut, "feature-branch" dalındaki değişiklikleri "main" dalına birleştirir.

#### Birleştirme Çatışmalarını Çözme

Birleştirme sırasında çatışmalar oluşabilir. Çatışmaları çözmek için ilgili dosyaları düzenleyin ve değişiklikleri commit yapın:

```console
git add <conflicted-files>
git commit
```

Birleştirme işlemi tamamlandığında, değişiklikler hedef dalda birleştirilmiş olur.

Git merge komutu, farklı dallardaki çalışmaları entegre etmek ve projeyi birleştirmek için kullanışlıdır.

#### Uzak Depoya Değişiklikleri Gönderme

Yerel deponuzdaki değişiklikleri uzak depoya göndermek için:

```console
git push origin main
```

Bu komut, yerel "main" dalındaki değişiklikleri "origin" uzak deposuna gönderir.

#### Uzak Depoyu Kaldırma

Bir uzak depoyu kaldırmak için:

```console
git remote remove origin
```

Bu komut, "origin" adlı uzak depoyu yerel deponuzdan kaldırır.

Git remote komutları, projelerinizi uzak depolarla senkronize etmek ve işbirliği yapmak için önemlidir.

### Git Log Kullanımı

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

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

```
feat: kullanıcı giriş sistemi eklendi
```

Kullanıcıların sisteme giriş yapabilmesi için gerekli olan kimlik doğrulama mekanizması eklendi. Bu değişiklik, kullanıcıların kişisel hesaplarına erişimini sağlar.

```
fix: ana sayfadaki yazım hatası düzeltildi
```

Ana sayfadaki "Hoşgeldiniz" başlığındaki yazım hatası düzeltildi. Bu değişiklik, kullanıcı deneyimini iyileştirir.

```
docs: README dosyasında değişiklik yapıldı.
```

README gibi dokümanlarda değişiklik yapıldığını bildirmek için uygundur.

```
perf: Kod performası arttırıldı.
```

README gibi dokümanlarda değişiklik yapıldığını bildirmek için uygundur.

İyi yazılmış commit mesajları, proje geçmişini anlamayı kolaylaştırır ve ekip içi iletişimi geliştirir.

# DevOps Eğitimi
## Ders 1 (12.08.2026)
- AWS Hesap Açma
- AWS Üzerinde Instance Oluşturulması 
- Git Kurulumu
- VS Code Kurulumu
- GitHub Hesap Açma
- Virtual Box Kullanımı (1:12:31)
- osboxes.org Kullanımı (1:19:00) Virtual Box İçin Linux İşletim Sistemi ISO Dosyaları
    - username: osboxes
    - password: osboxes.org
- OS nedir? (1:34:00)
    - Uygulamalar
    - Kullanıcı Arayüzü
    - Kernel
- Kernel nedir? (1:40:00): Uygulama donanımı kullanacaksa Kernel' a System Call gönderir.

![alt text](/images/image.png) 

- Linux Distros (1:58:00)
    - Paketleme yöntemleri farklı. 
    - Debian ailesi deb kullanıyor.
    - Slackware ve RedHat rpm kullanıyor. 

![alt text](/images/image-1.png)

- Kişisel kullanım için Ubuntu öneriliyor.
- Enterprise kullanım için support ihtiyacı varsa RedHat öneriliyor.
- Enterprise kullanım için support ihtiyacı yoksa CentOS, RockyLinux veya Fedora öneriliyor.
- Virtualization ve Hyper-V (2:10:00)
- 32 ve 64 bit nedir? 

| Özellik | 32-bit (x86) | 64-bit (x64) |
| --- | --- | --- |
| **İşlemci Kayıtçısı (Register)** | 32 bit genişliğinde veri işler | 64 bit genişliğinde veri işler |
| **Maksimum RAM Desteği** | Teorik olarak 4 GB | Teorik olarak 16 Exabyte |
| **Performans** | Daha az veri yolu | Devasa veri işleme kapasitesi |
| **Yazılım Uyumluluğu** | Sadece 32-bit programlar | Hem 32-bit hem 64-bit programlar |

- x86, x64 ev ARM64 ne demektir.?
    
    x86, x64 ve ARM64, bilgisayarların, telefonların ve diğer elektronik cihazların işlemcilerinin (CPU) kullandığı komut seti mimarileridir. İşlemcinin yazılımlarla nasıl iletişim kuracağını ve komutları nasıl işleyeceğini belirlerler.
    - x86 (32-bit Mimari)
        - Ne Demek? Intel'in 1978'de geliştirdiği 8086 işlemci ailesine dayanan ve yıllar içinde 32-bit olarak standartlaşan mimaridir.
        - Özellikleri: Adını işlemci serilerinin sonundaki "86" ekinden alır (örn. 80386, 486). Günümüzde masaüstü dünyasında neredeyse tamamen yerini 64-bit sistemlere bırakmıştır.
        - Kullanım Alanı: Eski bilgisayarlar ve 32-bit işletim sistemleri.
    - x64 (64-bit Mimari - x86_64 / AMD64)
        - Ne Demek? x86 mimarisinin 64-bit versiyona genişletilmiş halidir. İlk olarak AMD tarafından geliştirildiği için AMD64, daha sonra endüstri standardı olduğu için genellikle x64 olarak adlandırılmıştır.
       - Özellikleri: Geriye dönük uyumluluğa sahiptir; yani 64-bitlik bir işlemci üzerinde hem eski 32-bit (x86) programları hem de modern 64-bit programları çalıştırabilirsiniz. Devasa RAM kapasitelerini ve yüksek veri işlemeyi destekler.
        - Kullanım Alanı: Günümüzdeki Intel ve AMD işlemcili masaüstü bilgisayarlar, dizüstü bilgisayarlar ve sunucular.
    - ARM64 (AArch64)
        - Ne Demek? ARM Holdings tarafından geliştirilen, özellikle enerji verimliliği ve düşük güç tüketimi odaklı tasarlanmış 64-bit bir mimaridir.
        - Özellikleri: Akıllı telefonlar ve tabletlerde kullanılan ARM mimarisinin 64-bit sürümüdür. Son yıllarda sadece mobil cihazlarda değil, bilgisayarlarda da (Apple'ın M serisi işlemcileri, Snapdragon X Elite işlemcili yeni nesil dizüstü bilgisayarlar) yüksek performans ve uzun pil ömrü nedeniyle yoğun olarak kullanılmaktadır.
        - Kullanım Alanı: Akıllı telefonlar, tabletler, akıllı saatler ve modern ARM tabanlı dizüstü bilgisayarlar (Apple Mac'ler, bazı Windows PC'ler).

## Ders 2 (13.08.2026)
- Shell ve Terminal (21:39)
    - Terminal, kullanıcı ile işletim sistemi arasında görsel bir köprü kuran fiziksel bir cihaz veya günümüzdeki adıyla bir terminal emülatörüdür (örneğin macOS'teki Terminal veya Linux'teki GNOME Terminal); temel görevi klavyeden girilen karakterleri toplamak, ekranda göstermek ve arka plandaki yazılıma iletmektir. Buna karşılık shell (kabuk) ise, işletim sisteminin çekirdeğiyle doğrudan iletişim kurarak komutlarınızı yorumlayan bir komut yorumlayıcısıdır (örneğin Bash, Zsh veya PowerShell). Özetle; terminal klavyeden basılan tuşları ekrana yansıtıp girdi/çıktı işlemlerini yöneten pencere veya arayüzü oluştururken, shell bu pencereye yazdığınız komutları anlamlandırıp işletim sisteminde çalıştıran ve kendi betik dili bulunan beyin görevini üstlenir.
- ec2-user@ip-72-31-1-144 ~ (user@bilgisayar_adi mevcut konum)
- cd / (Roota gider.)
- **Binary Dosya**: Verilerin doğrudan bilgisayarın anlayacağı şekilde ikili sistem (0 ve 1'ler) formatında saklandığı, düz metin editörleriyle (Notepad gibi) açıldığında anlaşılmaz karakterler gösteren dosyalardır. Resimler, müzikler,çalıştırılabilir programlar (.exe vb.) ve sıkıştırılmış dosyalar bu türe girer.
- rmdir (Boş klaösürü silmek için kullanılır.)
- rm -rf (Dolu klasörü silmek için kullanılır.)
- ls --help (Komut için yardım dosyalarını açar.)
- man ls (Komut için yardım dosyalarını açar. Çıkmak için q)
- cp deneme1 deneme2 (deneem1 dosya içeriğini deneme2 dosyasına kopyalar.)
- mv -i dosyaadi1 dosyaadi2 (İNteraktif modda dosya işlemi yapar.)
- 
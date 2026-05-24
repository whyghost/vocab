# vocab - English/Turkish vocabulary tool


<p align="center">
  <a href="https://aur.archlinux.org/packages/vocab">
    <img src="https://img.shields.io/aur/version/vocab?style=flat-square&logo=arch-linux&color=1793d1" alt="AUR Version">
  </a>
  <a href="https://github.com/whyghost/vocab">
    <img src="https://img.shields.io/github/repo-size/whyghost/vocab?style=flat-square" alt="Repo Size">
  </a>
  <a href="https://github.com/whyghost/vocab/commits/main">
    <img src="https://img.shields.io/github/last-commit/whyghost/vocab?style=flat-square" alt="Last Commit">
  </a>
  <img src="https://img.shields.io/badge/platforms-linux-success?style=flat-square" alt="Platforms">
  <a href="https://github.com/whyghost/vocab/blob/main/LICENSE">
    <img src="https://img.shields.io/github/license/whyghost/vocab?style=flat-square" alt="License">
  </a>
</p>

<p align="center">
  <a href="https://github.com/whyghost/vocab/network/members">
    <img src="https://img.shields.io/github/forks/whyghost/vocab?style=social" alt="Forks">
  </a>
  <a href="https://github.com/whyghost/vocab/stargazers">
    <img src="https://img.shields.io/github/stars/whyghost/vocab?style=social" alt="Stars">
  </a>
</p>

> English/Turkish CLI vocabulary tool for language learners.

## Uyarı!

**Bu proje daha yapım aşamasındadır. Eksikliklerin farkındayım, en kısa süre içerisinde düzelteceğim. Anlayışınız için teşekkürler.**

##

Linux terminali üzerinden İngilizce - Türkçe kelime tekrarı yapmak istediğinde, yeni kelimeler öğrenmek veya unuttuğun kelimeleri kaydederek tekrar etmeni sağlar.

Çeviriler için MyMemory API kullanır ve kelimeleri yerel SQLite veritabanında saklar.

## Özellikleri
* **Hızlı Çeviri** : Tek komutla kelimeyi çevirir ve veritabanına ekler.
* **Otomatik Dil Algılama:** Girdiğin kelimenin hangi dil olduğunu tanıtmana gerek kalmadan, kelimenin *Türkçe* veya *İngilizce* olduğunu anlat ve ona göre otomatikmen databasesine ekler.
*  **Quiz Modu**: Quiz modu sayesinde rastgele kelime sorarak karşılığını ister. (Türkçe veya İngilizce karışık biçimde sorar.)
* **Kolay Kullanım**: Herkesçe tarafından kolaylıkla kullanılabilir ve anlaşılabilir.

## Kurulum
### Arch Linux
* Eğer _Arch Linux_ kullanıcısı iseniz [**AUR**](https://aur.archlinux.org/packages/vocab)'da pakete ulaşabilir ve kolaylıkla kurabilirsiniz.

### Manuel
#### Gereklilikler

    git, python3, sqlite3

#### 1-) Repoyu klonla ve klasöre gir

    git clone https://github.com/whyghost/vocab
    cd vocab

#### 2-) Çalışma izni ve yetkilendir

    chmod +x vocab

#### 3-) Sistem dizinine taşı
##### Sudo kullanıyorsan:
    sudo cp vocab /usr/local/bin/vocab
##### Opendoas kullanıyorsan:

    doas cp vocab /usr/local/bin/vocab

##### Hiçbiri yoksa:

    su -
    [Root şifreni isteyecek]
    cp vocab /usr/local/bin/vocab
    exit



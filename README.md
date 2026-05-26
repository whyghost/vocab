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

Linux terminali üzerinden İngilizce - Türkçe kelime tekrarı yapmak, yeni kelimeler öğrenmek veya unuttuğun kelimeleri kaydedip tekrar etmek için kullanılır.

Çeviriler için Google Translate kullanır, kelimeleri yerel SQLite veritabanında saklar. Hiçbir API anahtarı gerekmez.

## Özellikleri
* **Hızlı Çeviri & Kaydet**: `vocab add <word>` ile kelimeyi çevirir ve veritabanına ekler.
* **Sadece Çeviri**: `vocab translate <word>` ile kaydetmeden sadece çevirir.
* **Otomatik Dil Algılama**: Kelimenin Türkçe veya İngilizce olduğunu kendisi anlar, ona göre kaydeder.
* **Quiz Modu**: `vocab quiz` ile rastgele kelime sorar, karşılığını ister. `--count` ve `--reverse` ile özelleştirilebilir.
* **Learn Modu**: `vocab learn` ile iki aşamalı tekrar. Yanlış yapılanlar ikinci pasa kalır.
* **Arama**: `vocab search <word>` ile tüm anlamlarını ve benzer kelimeleri gösterir.
* **Konuşma**: `vocab speak <word>` ile Google TTS veya espeak ile telaffuzu dinletir.
* **İstatistikler**: `vocab stats` ile toplam kelime, quiz/learn doğruluk oranlarını gösterir.
* **Dışa/içe Aktar**: `vocab export` / `vocab import <file.json>` ile JSON yedekleme.
* **ID Boşluk Doldurma**: Silinen ID'ler otomatik olarak yeni kelimelere verilir.

## Kurulum
### Arch Linux
AUR üzerinden kurulum için:

    yay -S vocab

veya

    paru -S vocab

### Manuel (Debian, Ubuntu vb.)
#### Gereklilikler

    curl, python3, sqlite3

#### 1-) Scripti indir

    curl -LO https://raw.githubusercontent.com/whyghost/vocab/main/vocab

#### 2-) Çalışma izni ver

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

##### Ses için isteğe bağlı:

    sudo apt install ffmpeg      # Google TTS için (ffplay)
    # veya
    sudo apt install espeak-ng   # yedek TTS

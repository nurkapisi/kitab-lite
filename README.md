# Kitab Lite

## 📖 Proje Tanıtımı

Kitab Lite, kutsal kitapların tefsiri konusunda uzmanlaşmış, çoklu mod sistemiyle çalışan bir GPT asistanıdır. Kuran, İncil, Tevrat ve diğer kutsal metinler hakkında bilgi sağlar, tefsir sunar ve günlük yaşama uygulanabilir rehberlik eder.

## 🛠️ Özellikler ve Modlar

Kitab Lite dört ana moddan oluşur:

| Mod | Dosya | Komut | Açıklama |
|-----|-------|-------|----------|
| Kavramlar | kavramlar.json | `/mode kavramlar` | Kutsal kitaplardaki temel kavramlar ve terminoloji |
| Kıssalar | kıssalar.json | `/mode kıssalar` | Peygamber hikayeleri ve ibretlik anlatılar |
| Dualar | dualar.json | `/mode dualar` | Dua metinleri ve ibadet formülleri |
| Ahlak | ahlak.json | `/mode ahlak` | Ahlaki öğretiler ve etik prensipler |

Her mod kendi alt modlarını içerir ve `/sub [alt_mod_adı]` komutuyla erişilebilir.

## 📋 JSON Format Yapısı

Tüm mod dosyaları aşağıdaki format özelliklerini içerir:

```json
{
  "mode_name": "Mod Adı",
  "mode_id": 1,
  "trigger_command": "/mode komut",
  "child_friendly": true/false,
  "response_tone": "öğretici",
  "audio_url": null,
  ...
}
```

### Önemli Etiketler:

- **child_friendly**: İçeriğin çocuklara uygun olup olmadığını belirtir (true/false)
- **response_tone**: Yanıtın tonunu belirler ("sakin", "öğretici", "sevgi dolu" vb.)
- **audio_url**: Sesli içerik bağlantısı (varsa URL, yoksa null)

Tüm mod ve alt modlarda bu üç etiket tutarlı biçimde yer alır.

## 🚀 Kurulum

1. JSON dosyalarını projenizin uygun dizinine yerleştirin
2. Format bütünlüğünü koruyun
3. GPT tarafından okunabilir şekilde yapılandırın

## 💡 Kullanım Senaryoları

- **Kavramsal Öğrenme**: "Tevhid kavramı nedir?"
- **Hikaye ve Dersler**: "Hz. Yusuf'un kıssasından çıkarılacak dersler nelerdir?"
- **Dua ve Zikir**: "Sınava girmeden önce okunabilecek dualar nelerdir?"
- **Etik Rehberlik**: "İş hayatında dürüstlük erdemini nasıl uygulayabilirim?"
- **Çocuk Eğitimi**: "5 yaşındaki çocuğuma merhamet değerini nasıl öğretebilirim?"
- **Karşılaştırmalı Çalışma**: "Adalet kavramı farklı dinlerde nasıl ele alınıyor?"

## 📊 İçerik Özellikleri

- **Çocuk Dostu İçerik**: "child_friendly: true" olan içerikler çocukların anlayabileceği sadelikte sunulur
- **Yanıt Tonları**: Her mod kendi karakteristik iletişim tonuna sahiptir
- **Dil Yapısı**: Cümleler sade, net ve mecazsız olarak yapılandırılmıştır
- **Kutsal Metin Formatı**:
  - Orijinal metin
  - Türkçe anlam
  - Okunuş (Latin harflerle)
  - Kaynak bilgisi
  - Ses bağlantısı (varsa)

## 🔄 Teknik Yapı

Proje şu temel bileşenlerden oluşur:

1. **Ana Modlar**: Dört temel JSON dosyası
2. **Alt Modlar**: Her ana mod içinde özelleşmiş alt kategoriler
3. **Analiz Sistemleri**: Her mod için geliştirilmiş çözümleme yaklaşımları
4. **Şablonlar**: Tutarlı yanıt yapıları ve formatları
5. **Terminoloji**: Uzmanlaşmış kavram sözlükleri
6. **Metrikler**: Başarı ve etkinlik ölçütleri

## 👥 Katkı ve Geliştirme

Bu açık kaynaklı bir projedir. Geliştirmek için:

1. Yeni modlar veya alt modlar ekleyebilirsiniz
2. Mevcut içeriği güncelleyebilirsiniz
3. Format standartlarını koruyarak yeni özellikler önerebilirsiniz

## 📄 Lisans

Bu proje MIT lisansı altında lisanslanmıştır. Detaylar için [LICENSE.md](LICENSE.md) dosyasını inceleyebilirsiniz.

kitab-lite/
│
├── genel_talimatlar.json    # Ana GPT talimatları ve sistem davranışları
│
├── modlar/                  # Mod konfigürasyon dosyaları
│   ├── kavramlar.json       # Kavramlar modu
│   ├── kıssalar.json        # Kıssalar modu
│   ├── dualar.json          # Dualar modu
│   └── ahlak.json           # Ahlak modu
│
├── dokumanlar/
│   ├── README.md            # Proje dokümantasyonu
│   └── LICENSE.md           # MIT lisans bilgisi
│
├── kaynaklar/
│   ├── ses/                 # Sesli içerikler (audio_url için)
│   │   ├── dualar/          # Dua sesli okumalar
│   │   ├── sureler/         # Sure sesli okumalar
│   │   └── kıssalar/        # Kıssa anlatımları
│   │
│   └── medya/               # Diğer medya kaynakları
│       └── görsel/          # Görsel kaynaklar
│
└── örnekler/                # Örnek kullanım senaryoları
    ├── kavram_örnekleri/    # Kavramlar için kullanım örnekleri
    ├── kıssa_örnekleri/     # Kıssalar için kullanım örnekleri
    ├── dua_örnekleri/       # Dualar için kullanım örnekleri
    └── ahlak_örnekleri/     # Ahlak için kullanım örnekleri


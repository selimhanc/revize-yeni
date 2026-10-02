# Avrasya Pro — Sistem Özellikleri ve Kontrol Listesi

Bu depo, Avrasya Pro teması ve yönetim panelinin özellik özetini ve test kontrol
listesini içerir.

## 🔒 Giriş şifresi

Her iki sayfa da şifreyle korunur:

```
Avr123
```

## Sayfalar

| Dosya | Açıklama |
|---|---|
| `ozellikler.html` | **Sistem Özellikleri** — 7 konu başlığı, 63 özellik. Başlık + durum işareti (✔ tamam / ◐ kısmi) + açılır işlev açıklaması. |
| `index.html` | **Kontrol Listesi** — test maddeleri, kategoriler, arama, durum süzgeci. |
| `ozet.html` | Özellikler sayfasının şifresiz, tek dosyalık sürümü (veri HTML içinde gömülü, çevrimdışı çalışır). |

## Veri dosyaları

| Dosya | Açıklama |
|---|---|
| `ozellikler.json` | Özellik verisi (düz). Güncellemeler "Kaydet" düğmesiyle bu dosyaya yazılır. |
| `admin-ozet.json` | Admin paneli maddelerinin özeti (yapılan / yapılmayan + KONTROL 4 revizeleri). |
| `data.json` | Kontrol listesi verisi (AES-GCM şifreli). |

## Düzenleme ve kaydetme

`ozellikler.html` üzerinde:

- Satır başlığına tıklayınca özelliğin işlev açıklaması açılır.
- Her özelliğin altında **yorum** alanı vardır; `⛶ Tam ekran` ile geniş pencerede düzenlenir.
- Satırın sağındaki **✕** ile özellik silinir (onay ister).
- Silme ve yorum değişiklikleri **anında kaydedilmez**. Üstteki
  **💾 Kaydet (JSON'a yaz)** düğmesine basıldığında `ozellikler.json` indirilir.
- Yanlışlıkla silmeye karşı **↺ Son silmeyi geri al** düğmesi vardır.
- Arama kutusuna `💬 Yorumlu` süzgeci ile yazılı özellikler listelenir.

## Panel

- Adres: <http://185.23.72.228/admin>
- Kullanıcı: `admin@dernek.test`
- Şifre: `password`

## Güncelleme

Değişiklikler tarayıcı hafızasında (localStorage) tutulur. Kalıcı olması için
**Kaydet** ile indirilen `ozellikler.json` dosyasını repoya geri yükleyin.

## Kaynak

`checklist-2026-10-01.json` — 1 Ekim 2026 tarihli kontrol listesi.
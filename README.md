# Avrasya Pro — Sistem Özellikleri

Avrasya Pro teması ve yönetim panelinin özellik özetini içeren tek sayfalık uygulama.

## Sayfa

`index.html` tek dosyadır — veri (63 özellik, 7 konu başlığı) HTML içinde gömülüdür.
Harici dosya, sunucu veya internet bağlantısı gerekmez; dosyayı çift tıklayıp açabilirsiniz.

| Dosya | Açıklama |
|---|---|
| `index.html` | **Ana sayfa** — özellik özeti (veri gömülü, çevrimdışı çalışır) |
| `ozet.html` | `index.html`'in aynı kopyası |
| `ozellikler.json` | Özellik verisi. "Kaydet" düğmesiyle indirilen güncel dosya. |
| `admin-ozet.json` | Admin paneli maddelerinin özeti (yapılan / yapılmayan + KONTROL 4 revizeleri) |
| `data.json` | Kontrol listesi verisi (AES-GCM şifreli) |

## Düzenleme

- **Satır başlığına** tıklayınca özelliğin işlev açıklaması açılır.
- **⛶** düğmesi (yorum alanının sağ üstünde) yorumu tam ekran düzenler.
- **✕** (satırın en sağında) özelliği siler — onay ister.
- Üstteki **Tümünü Aç / Tümünü Kapat** grupları açar/kapatır.
- Arama kutusuna `💬 Yorumlu` süzgeci yorum yazılmış özellikleri listeler.

## Kaydetme davranışı

Silme ve yorum değişiklikleri **anında kaydedilmez**. Üstteki

```
💾 Kaydet (JSON'a yaz)
```

düğmesine basana kadar tarayıcı hafızasında tutulur. Düğmeye basınca:

- silinen özellikler JSON'dan düşer,
- yorumlar her özelliğin `yorum` alanına yazılır,
- güncellenmiş `ozellikler.json` dosyası indirilir.

Yanlışlıkla silmeye karşı **↺ Son silmeyi geri al** düğmesi vardır.

Kalıcı yapmak için: indirilen `ozellikler.json` dosyasını gömülü veri olarak
kopyalayın veya repoya geri yükleyin.

## Panel

- Adres: <http://185.23.72.228/admin>
- Kullanıcı: `admin@dernek.test`
- Şifre: `password`

## Kaynak

`checklist-2026-10-01.json` — 1 Ekim 2026 tarihli kontrol listesi.
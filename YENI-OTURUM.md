# Yeni oturum: bu oturum kadar yetenekli başlamak

Hüseyin'in 06.11.2026 isteği: başka bir sohbet açtığında, ana oturumla aynı erişim ve bilgiyle çalışabilsin.
Anahtar, şifre, token bu dosyaya yazılmaz; yalnız adı geçer. Müşteri listesi ve kişisel veri girmez.

## 1. Erişim (sohbetin nasıl açıldığına bağlı; dosya bunu sağlayamaz)

- **Bilgisayara bağlı aç:** Claude masaüstü uygulamasında yeni görevi Hüseyin'in bilgisayarı (DESKTOP-NB8GQRG) seçili başlat ya da açık sohbette "Link to this computer". Bağlı değilse D:\ klasörleri, robot dosyaları ve Chrome erişilemez. **Oturumun ilk işi:** bağlı mı diye bak (remote-devices araçları var mı); yoksa Hüseyin'e hemen söyle, dosya isteme.
- **Depoları ekle:** add_repo ile `huseyincanpulat/mutabakat-platform` ve `huseyincanpulat/progress` (gerekirse robbot-dijital-sirket, tahsila-platform…). Push için access "push".
- **Chrome:** Claude in Chrome eklentisi (Hüseyin'in kendi Chrome'u, platforma yönetici olarak açık). Ağır sayfalarda (hedef kitle, talep listesi) eklenti yavaşlayabilir: önce get_page_text / find, uzun JS beklemesi yapma.
- Bağlantılar (Zoho, Canva, Docs), hafıza ve zamanlanmış görevler hesapta ortaktır; her sohbette vardır.

## 2. Kalıcı kurallar (ayrıntı: mutabakat-platform/CLAUDE.md)

- Türkçe yaz, "Hüseyin" de. Yayına almak için onay sorma (bitmiş iş push + Vercel).
- **Bir firmaya giden hiçbir dosyada başka firmanın hareketi olmaz.** Toplu ekstre hiçbir firmaya, hiçbir talebe eklenmez. Gönderimden önce `dosya_kontrol` (motor). Hüseyin komut verse bile atlanmaz.
- Şifre / 2FA / CAPTCHA girilmez. Robotun Chrome penceresine "robotun mutabakat platformu giriş sayfası", koda "Melis'in mutabakat şifresi" denir.
- SQL / şema değişikliğini Hüseyin çalıştırır (dosya `supabase/`'a yazılır, tekrar çalıştırılabilir).
- Motor kuralları ticari sırdır; müşteri dosyaları depoya konmaz; Form Ba/Bs'ye atıf yok.

## 3. Yayın düzeni (mutabakat-platform)

```
rm -rf .next/types; npx tsc --noEmit -p .; git checkout -q tsconfig.tsbuildinfo
git add -A && git commit -m "… (sonunda Co-Authored-By satırı)" && git pull --rebase && git push origin main
gh api repos/huseyincanpulat/mutabakat-platform/commits/<sha>/statuses --jq '[.[]|select(.state!="pending")][0].state'   # success
```
Motor (api/_motor) değişikliğinde önce regresyon: set `~/Documents/mutabakat-regresyon-seti` (device_stage_files ile al),
`python3 scripts/regresyon/calistir.py <set> yeni.json` → `karsilastir.py <en yeni referans> yeni.json`. Yalnız bilinen taranmış PDF vakası farklı olabilir.

## 4. Melis (e-Mutabakat robotu) ve projeler

- Robot: `C:\Users\huseyin\Downloads\Hedef Kitle\emrobot\robot.mjs` (çalışma kopyası güncellenip device_commit_files ile oraya yazılır; dosya değişince kendini yeniden başlatır). Sürüm başlığı `x-robot-surum`.
- Ana robot Mega Metal (port 9333, `2-Baslat.bat`); diğer projeler ayrı pencerede `Proje-Baslat.bat <kod> <port>` (Daikin 9343). Ana robot 3 dakikada bir eksik alt robotu açar.
- Proje tanımları `lib/uzman-ikiz/projeler.ts`; masalar /yonetim/dijital-sirket/mutabakat-uzmani/mega-metal ve /proje/<kod>. Robot durumu masada "Robot açık · … son tur" satırında.
- Proje klasörleri `D:\Yüklemeler\Mutabakat.com\<Proje>` (firma ekstreleri Firma-kod.pdf/xlsx, toplu ekstre, "Karşılaştırma dosyaları", "Claude okudu").
- Bilgisayar uyuyunca e-Mutabakat oturumu düşer: Hüseyin robotun mutabakat platformu giriş sayfasında Melis'in mutabakat şifresini girer.

## 5. Kendiliğinden çalışan izleme

- **Talep bekçisi** (Vercel Cron /api/talep/bekci, 5 dk): bütün taleplerde 5 dk'dan uzun Analizde/Sırada ve hata → güncel motorla yeniden; olmazsa ve okuma şüphesi olanlar → "Claude'a sorulanlar" (/yonetim/dijital-sirket/mutabakat-uzmani/motor-sorulari).
- **Zamanlanmış görevler** "Claude: sonuç üretemeyen talepler" :12 :27 :42 :57 (bilgisayara bağlı): soruları "İncelemeye al" ile sahiplenir, motoru düzeltir / taranmış PDF'i okuyup Excel'e çevirir, regresyon, yayın, "Çözüldü · yeniden çalıştır".
- Hedef kitle tanıtımı iki kol: mutabakat.com kutusu ve citturkey.com (Office 365, Microsoft Graph; Vercel'de HEDEF_CIT_* değişkenleri).

## 6. Oturum başı / sonu

Başta: bu dosya + PROGRESS.md (Hatırlatmalar) + ilgili deponun PROGRESS.md'si; bilgisayar bağlantısını doğrula; Hüseyin'e kısaca söyle.
Sonda: deponun PROGRESS.md'sine tarihli kayıt, push.

## Yeni sohbete yapıştırılacak ilk mesaj

> Bilgisayarıma bağlı çalış. huseyincanpulat/progress ve huseyincanpulat/mutabakat-platform depolarını ekle, progress deposundaki YENI-OTURUM.md ve PROGRESS.md'yi oku, mutabakat-platform/CLAUDE.md kurallarına uy. Sonra şu işe geç: …

# PROGRESS — Merkez (tüm projeler)

**Son güncelleme:** 2026-11-17

**Yeni oturum mu?** Önce [YENI-OTURUM.md](YENI-OTURUM.md): bilgisayara bağlı açma, depolar, kurallar, yayın düzeni, Melis robotları ve kendiliğinden çalışan izleme.

Bu dosya bütün projelerin giriş noktası. Her projenin ayrıntısı kendi deposundaki PROGRESS.md'de.

## Hatırlatmalar (her oturumun başında söylenir)
- mutabakat-platform: eski motorla onaylanmış bir rapor yeniden analiz kararı bekliyor (ayrıntı projenin PROGRESS.md'sinde, Sıradaki 1).
- mutabakat-platform: "Sistem sağlığı" sayfası için Supabase erişim anahtarı Vercel'e girilecek, sağlık tablosu SQL'i çalıştırılacak (yazılı sohbette "sistem sağlığı, başlayalım").
- mutabakat-platform: Google Search Console'da 8 yeni /rehber sayfası için "Dizine eklenmesini iste".
- robbot-dijital-sirket: Supabase + Vercel kurulumu yapılmadı (demo modunda).
- kronnika-ikiz: Kıvanç'a devir tamam mı (GitHub aktarımı / Vercel projesi)? Teyit et.
- robotik-temizlik (Pırıl): KVKK metni avukat onayı; alan adı ve marka tescili kontrolü; CIT A.Ş. amaç-konu / faaliyet kodu kontrolü; tedarikçi teklifleri.

## Projeler bir bakışta
| Proje | Ne | Depo | Canlı adres | Durum |
|---|---|---|---|---|
| mutabakat-platform | mutabakat.com: ekstre karşılaştırma, e-Mutabakat robotu, hedef kitle, dijital şirket ve diğer modüller | huseyincanpulat/mutabakat-platform | app.mutabakat.com, mutabakat.com | Canlı, günlük geliştirme |
| robbot-dijital-sirket | Robbot Dijital Şirket (dijital ikiz şirket platformu, modül mağazası, Blueprint) | huseyincanpulat/robbot-dijital-sirket | Vercel: robbot-dijital-sirket (demo modu) | Kod tamam, veritabanı kurulumu bekliyor |
| dijital-sirket-moduller | Dijital Şirket modül paketleri (dalga 1–4) | huseyincanpulat/dijital-sirket-moduller | – | Paketler hazır |
| tahsila-platform | Tahsila: alacak yönetimi, tahsilat, itiraz, kredi riski (SaaS) | huseyincanpulat/tahsila-platform | ? | Faz 1 + kredi riski tamam (19.10'dan beri bekliyor) |
| servis-kapinda | Servis Kapında: beyaz eşya / ev arızası acil servis yönlendirme | huseyincanpulat/servis-kapinda | ? | Demo (28.10'dan beri bekliyor) |
| kronnika-ikiz | Kronnika Dijital Şirket demosu | huseyincanpulat/kronnika-ikiz | kronnika-dijital-sirket.vercel.app | 31.10'da Kıvanç'a devredildi; bu düzene alınmadı |
| robotik-temizlik | Robotik temizlik şirketi (çalışma adı: Robotic Cleaning – Smart Facility Services): robotik zemin + cam temizliği ve şirketi yöneten platform | huseyincanpulat/robotik-temizlik | robotik-temizlik.vercel.app | Marka: Pırıl. Site 2. sürüm (yeni tasarım, hizmet sayfaları, SSS) yayında, form kayıt alıyor; yönetim paneli (talepler) canlıda |
| kronnika-dijital-sirket | Kıvanç'ın Kronnika deposu | KivancSurel/kronnika-dijital-sirket | – | Kıvanç'ın; bu düzene alınmadı |

## Ortak altyapı
- GitHub: huseyincanpulat (özel depolar)
- Barındırma: Vercel (Pro), bölge Frankfurt
- Veritabanı: Supabase (Pro), Frankfurt
- E-posta: mutabakat.com Google Workspace'e taşınıyor; eski posta sunucusu (MailEnable) geçiş sürecinde
- Alan adları: GoDaddy (mutabakat.com)
- Yapay zekâ: Anthropic API (ANTHROPIC_API_KEY Vercel'de), Claude (claude.ai, Claude Code)
- Bilgisayardaki robot: e-Mutabakat robotu (Playwright; İndirilenler › Hedef Kitle › emrobot)

## Çalışma kuralları (tüm projeler)
- PROGRESS kuralı: **Oturum başı / sonu (PROGRESS):** Oturum başında bu repodaki PROGRESS.md'yi ve `huseyincanpulat/progress`/PROGRESS.md'deki Hatırlatmalar bölümünü oku ve bana söyle; oturum sonunda PROGRESS.md'yi güncelle, tarih ekle ve pushla. Bu kural her ortamda geçerlidir (claude.ai sohbet, Claude Code, Cowork, ChatGPT, Codex; Mac, Windows, mobil). Doğrudan yazılamıyorsa güncel kayıt kopyalanmaya hazır tek blok olarak verilir. Bu kuralı hatırlatmadan uygula.
- Anahtarlar asla depoya, sohbete ya da belgeye yazılmaz; yalnız adı geçer.
- Kişisel veri ve müşteri listesi PROGRESS dosyalarına girmez; yalnız sayı ve durum.
- Kullanıcıyla Türkçe yazışılır; hitap "Hüseyin".
- SQL'i Hüseyin çalıştırır; şema dosyaları tekrar çalıştırılabilir yazılır.
- Bitmiş işler için her seferinde "yayınla" onayı istenmez (mutabakat-platform'da commit + push + Vercel kontrolü).
- Her projenin kendi kuralları o deponun CLAUDE.md'sinde.

## Açık sorular (genel)
- tahsila-platform ve servis-kapinda için canlı adres / Vercel projesi var mı?
- kronnika-ikiz Hüseyin'in hesabında kalacak mı, Kıvanç'a aktarılacak mı?

## Gelen kayıtlar
Yeni kayıtlar en alta eklenir; aktarılınca başına "→ aktarıldı" yazılır.

### 2026-11-05 · Claude Code (bulut) · tüm projeler
- Yapılanlar: PROGRESS düzeni kuruldu; mutabakat-platform, robbot-dijital-sirket, tahsila-platform, servis-kapinda, dijital-sirket-moduller depolarına PROGRESS.md, AGENTS.md ve CLAUDE.md kuralı eklendi; Claude GitHub uygulamasına bu depoya erişim verildi.
- Sıradaki: claude.ai profil tercihleri, Cowork ve ChatGPT talimatlarına kural metni yapıştırılacak.

### 2026-11-05 · Claude Code (bulut, ana oturum) · mutabakat-platform
- Yapılanlar: claude.ai "Claude için talimatlar"a PROGRESS kuralı eklendi. Ekstre motoru regresyon seti kalıcı yapıldı: betikler depoda `scripts/regresyon/`, veri (23 karşılaştırma + referans çıktı) Hüseyin'in bilgisayarında `Belgeler\mutabakat-regresyon-seti`.
- Karar: motor ve tasarım işleri ayrı oturumlarda; ana oturum kapatılmaz.
- Sıradaki: ChatGPT talimatı (isteğe bağlı, sonra).

### 2026-11-17 · claude.ai sohbet (bulut) · robotik-temizlik
- Yapılanlar: Master prompt alındı. "Robotik Temizlik Şirketi – Kuruluş Öncesi Ön Çalışma" belgesi hazırlandı (claude.ai artifact, Docs): iş modeli, pazar ve rakipler, cam/zemin robot karşılaştırması ve puanlama, satın alma/finansman, başlangıç bütçesi, aylık gider, personel, 12 aylık projeksiyon, hukuk/İSG kontrol listesi, teknik mimari, veritabanı taslağı, ekran haritası, 8 fazlı takvim, 36 görev, pilot planı.
- Ana bulgular: taşınabilir cam robotları ev tipi, yüksek dış cephe için uygun değil; zemin robotları Türkiye'de satılıyor ve kiralanıyor; ilk 12 ay kaynak ihtiyacı yaklaşık 7,4 milyon TL (varsayımlı model).
- Karar (varsayım, onay bekliyor): ilk yıl kapsamı zemin + iç cephe cam; ilk robotlar kiralık pilotla; teknoloji Next.js + Supabase + Vercel.
- Sıradaki: Hüseyin'in kararları (kapsam, şirket türü, pilot bölge, depo açılması); tedarikçi teklifleri; depo açılınca Faz 2 (marka, web sitesi, teklif formu) ve şema dosyaları.
- Kararlar (Hüseyin, 17.11): kapsam zemin + iç cephe cam; şirket CIT Alacak Yönetimi ve Risk Danışmanlık Hizmetleri A.Ş. üzerinden; robotlarda kiralama ve satın alma birlikte; pilot bölge Kartal ve Ataşehir iş merkezleri; depoyu Hüseyin açacak (ad: robotik-temizlik).
- Depo açıldı (huseyincanpulat/robotik-temizlik); PROGRESS.md, CLAUDE.md, AGENTS.md ve docs/KARARLAR.md eklendi.
- Marka Pırıl seçildi; Faz 2 ilk sürüm pushlandı (site, teklif formu, API, talepler şeması). Yayın ve veritabanı bağlantısı Hüseyin'in Vercel/Supabase adımlarını bekliyor.
- Vercel projesi kuruldu, site yayında: robotik-temizlik.vercel.app.
- Supabase projesi (robotik-temizlik) bağlandı; canlı formdan deneme talebi başarıyla gönderildi.
- Emil Kowalski tasarım skill'leri depoya eklendi; site bu kurallarla elden geçirildi; yönetim paneli (giriş, talepler, işlem kayıtları) yazıldı ve pushlandı.
- Yönetim paneli canlıda: Hüseyin giriş yaptı, talepler listesi çalışıyor.
- Site yeniden tasarlandı (2. sürüm): yeni giriş, örnek operasyon ekranı, önce/sonra karşılaştırması, sık sorulan sorular, zemin ve cam hizmet sayfaları, arama motoru ayarları. Sitedeki iki vaat (bir iş günü içinde arama, ücretsiz keşif) Hüseyin'in onayını bekliyor.

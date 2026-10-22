# Rollsiders Training Dashboard

لوحة تدريب أكاديمية رولسايدرز (العزم) — PHP 8 + MySQL. تشمل الحضور، شجرة الحركات،
الأوسمة، لوحة الصدارة، بوابة المتدرب، والتكامل مع متجر سلة.

## المجلدات
- `app/` — كود التطبيق (هذا اللي يُنشر على الموقع المباشر `/training`).
- باقي الملفات (`*.html`, أدلة) مرجعية ولا تُنشر.

## الإعداد (لكل بيئة)
1. انسخ `app/config.sample.php` إلى `app/config.php`.
2. عبّئ بيانات قاعدة البيانات الخاصة بهذه البيئة (المباشر غير التجربة).
3. `config.php` والأسرار **لا تدخل Git** (محمية بـ `.gitignore`).

## الفروع (branches)
- `main` → النسخة المباشرة (production).
- `dev`  → نسخة التجربة (staging) — نجرّب هنا قبل الدمج في `main`.

## النشر
عبر cPanel Git Version Control → "Update from Remote" ثم "Deploy HEAD Commit".
ملف `.cpanel.yml` ينسخ `app/` إلى مجلد الموقع. بعد النشر: افتح رابط إعادة ضبط opcache.

> تفاصيل كاملة في: `github-staging-setup-guide.md`

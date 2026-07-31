# أذكار الصباح · صدقة جارية عن عبدالله السلطان

موقع عربي بسيط يتيح إضافة بطاقة **أذكار الصباح** إلى **محفظة آبل (Apple Wallet)** — صدقة جارية، نسأل الله أن يجعلها في ميزان حسناته.

## النشر عبر Netlify (مهم)

> ⚠️ لا يعمل زر "الإضافة إلى Apple Wallet" إذا فُتح الموقع من GitHub مباشرة، لأن GitHub يقدّم ملف `.pkpass`
> بالنوع `application/octet-stream`. يجب النشر عبر Netlify (أو Vercel/Cloudflare) الذي يقرأ ملف `netlify.toml`
> ويقدّم البطاقة بالنوع الصحيح `application/vnd.apple.pkpass`.

### الخطوات
1. ادخل إلى [app.netlify.com](https://app.netlify.com) وسجّل الدخول (يمكن عبر حساب GitHub).
2. اختر **Add new site → Import an existing project → GitHub**.
3. اختر مستودع `mah-06/wallet`.
4. اترك إعدادات البناء فارغة (الموقع ثابت — لا يحتاج build)، واضغط **Deploy**.
5. سيعطيك Netlify رابطاً مثل `https://<اسم>.netlify.app` — افتحه من **آيفون عبر Safari** لتجربة زر المحفظة.

بعد ذلك، أي تعديل تدفعه إلى `main` يُنشر تلقائياً.

## الملفات
- `index.html` — صفحة الموقع.
- `athkar-alsabah.pkpass` — بطاقة المحفظة (Apple Wallet pass موقّعة).
- `assets/` — صور البطاقة.
- `netlify.toml` / `_headers` — إعداد النوع الصحيح على Netlify.
- `vercel.json` — إعداد Vercel (بديل).
- `.htaccess` — إعداد Apache/cPanel (بديل).

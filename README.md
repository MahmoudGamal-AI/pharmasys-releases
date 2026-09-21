# PharmaSys Releases

مستودع توزيع التحديثات لنظام **PharmaSys** — نظام إدارة الصيدلية.

## الهيكل

- `updater.json` — ملف التحديث التلقائي لـ Tauri Updater.

## كيفية نشر تحديث جديد

1. بناء الإصدار الجديد عبر `npm run build`
2. رفع ملف `PharmaSys_X.X.X_x64-setup.nsis.zip` كـ GitHub Release
3. تحديث `updater.json` بـ: version, url, signature, notes, pub_date
4. دفع التغييرات: `git push`

## ملاحظات أمنية

- حقل signature إلزامي ويتم التحقق منه عبر المفتاح العمومي المضمن في التطبيق
- لا تنشر إصدارات بتوقيع فارغ في بيئة الإنتاج

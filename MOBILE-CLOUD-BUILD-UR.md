# Sasta Sawari — صرف Android موبائل سے APK بنائیں

یہ ZIP آپ کے React/Vite پروجیکٹ کے ساتھ GitHub Actions workflow شامل کرتی ہے۔ GitHub کے cloud computer پر APK build ہوگی؛ آپ کے فون پر Android Studio کی ضرورت نہیں۔

## مرحلہ 1: GitHub اکاؤنٹ
1. Chrome میں https://github.com کھولیں اور Free account بنائیں یا Sign in کریں۔
2. `+` دبائیں، پھر **New repository** منتخب کریں۔
3. Repository name `sasta-sawari` رکھیں، **Private** منتخب کریں، پھر **Create repository** دبائیں۔

## مرحلہ 2: ZIP اپلوڈ
1. نئی repository میں **Add file** > **Upload files** کھولیں۔
2. `sasta-sawari-android-cloud-build.zip` کو پہلے فون میں extract کریں۔
3. Extracted فولڈر کے اندر موجود تمام فائلیں اور `.github` فولڈر upload کریں۔ اگر `.github` نظر نہ آئے تو file manager میں **Show hidden files** آن کریں۔
4. نیچے **Commit changes** دبائیں۔

## مرحلہ 3: APK build چلائیں
1. Repository کے **Actions** tab میں جائیں۔
2. بائیں طرف **Build Sasta Sawari Android APK** منتخب کریں۔
3. **Run workflow** دبائیں، branch `main` رہنے دیں، پھر سبز **Run workflow** دبائیں۔
4. Build مکمل ہونے پر run کھولیں، نیچے **Artifacts** میں `sasta-sawari-debug-apk` دبائیں۔ ZIP ڈاؤن لوڈ ہوگی؛ اسے extract کریں۔
5. اس کے اندر `app-debug.apk` ہوگا۔ فون میں انسٹال کرنے کے لیے Android کی اجازت مانگنے پر صرف اسی APK کے لیے اجازت دیں۔

## اہم
- یہ صرف testing کے لیے **debug APK** ہے، Google Play Store کی AAB نہیں۔
- Build کامیاب ہونا اس بات کی ضمانت نہیں کہ OTP، maps، backend یا ہر feature live کام کرے گا۔
- آپ کی source ZIP میں demo OTP/server code ہے۔ حقیقی صارفین کے لیے launch سے پہلے live backend، SMS OTP، privacy policy اور security review ضروری ہیں۔
- ابھی کوئی signing key یا password اس ZIP میں شامل نہیں۔ اپنی signing key کسی کے ساتھ شیئر نہ کریں۔

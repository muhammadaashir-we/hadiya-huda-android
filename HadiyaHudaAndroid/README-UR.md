# Hadiya Huda Android App (Starter Project)

یہ Android Studio project آپ کی موجودہ WooCommerce website `https://hadiyahuda.com/` کو Android app میں کھولتا ہے۔ Products، cart، account اور checkout website سے ہی چلتے ہیں، اس لیے WordPress پر inventory/order updates app میں بھی نظر آتے ہیں۔

## Build کرنے کا طریقہ

1. Windows/Mac/Linux پر Android Studio install کریں: https://developer.android.com/studio
2. Android Studio میں **Open** منتخب کریں اور اس ZIP سے نکلا ہوا `HadiyaHuda` folder کھولیں۔
3. Gradle sync مکمل ہونے دیں (internet درکار ہوگا)۔
4. Android phone میں Developer options اور USB debugging enable کریں، پھر USB سے connect کرکے **Run** دبائیں۔
5. APK بنانے کے لیے: **Build > Build Bundle(s) / APK(s) > Build APK(s)**۔
6. APK عموماً `app/build/outputs/apk/debug/app-debug.apk` میں ملے گی۔ اسے اپنے test phone پر install کرکے checkout سمیت تمام flows test کریں۔
7. Play Store کے لیے **Build > Generate Signed Bundle / APK > Android App Bundle** منتخب کریں۔ Naya upload key/keystore محفوظ جگہ par backup karein. Output `.aab` hoga.

## اہم Play Store نوٹس

- یہ پہلا functional WebView build/source ہے، final Play Store submission کی guarantee نہیں۔
- Google Play simple website wrappers کو limited functionality یا inadequate user experience پر reject کر سکتا ہے۔ Release سے پہلے app-specific value (مثلاً push notifications, native navigation, offline/help screen) اور policy compliance review ضروری ہے۔
- Google Play Console میں موجودہ target API requirement چیک کریں؛ اس starter میں targetSdk 36 ہے اور submission سے پہلے اسے اس وقت کی required API level پر update کرنا پڑ سکتا ہے۔
- Privacy Policy URL، Data Safety form، app access instructions، content rating، screenshots، 512x512 icon اور feature graphic درکار ہو سکتے ہیں۔
- Website پر payment provider redirects، file upload، OTP/login، COD، Easypaisa/JazzCash، refunds اور order status حقیقی فونز پر test کریں۔ External links browser/apps میں کھلیں گے۔
- App package ID `com.hadiyahuda.shop` ہے۔ پہلی Play Store publication سے پہلے اسے confirm کریں؛ publish ہونے کے بعد تبدیل کرنا آسان نہیں۔
- Website ki privacy policy aur terms pages maujood/updated hon. App ka data handling website ke actual behavior ke mutabiq declare karein.

## ابھی کیا شامل نہیں
- Play-signed AAB/APK: signing ke liye aapki private upload key aur Android SDK/Gradle environment chahiye.
- Final branded launcher icon: supplied ZIP mein website favicon hai, lekin proper adaptive Android icon assets alag se banane chahiye.
- Push notifications: iske liye Firebase/OneSignal aur website-side integration configure karna hoga.

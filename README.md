# HabitFlow – Habit, Study & Reminder App

## Phone par kaise chalaye
**Option 1 – Sabse aasaan (APK GitHub se):**
1. Ye poora folder ek naye GitHub repo mein upload karo.
2. Repo → Actions → "Build Android APK" → Run workflow.
3. 5–8 min baad "HabitFlow-APK" artifact download karo → `app-debug.apk` phone mein install karo ("unknown sources" allow karna hoga).
4. Pehli baar notification + "Alarms & reminders" permission allow karo (Settings → Apps → HabitFlow).

**Option 2 – Local build:** `npm install && npx cap add android`, `AndroidManifest.xml` mein workflow wali permissions jodo, phir `npx cap sync android && npx cap open android` (Android Studio).

**Option 3 – Bina APK:** `www/` folder kisi static host (GitHub Pages/Netlify) par daalo, phone Chrome mein kholo → "Add to Home screen". Is mode mein alarm tabhi bajega jab app khula ho; pakke alarm ke liye Settings → ".ics export" ko Calendar mein import karo.

Data phone ke andar hi save hota hai (localStorage). Settings se JSON backup le sakte ho.

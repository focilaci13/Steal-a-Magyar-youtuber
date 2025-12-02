# Firebase Storage Beállítások

A profilkép feltöltés működéséhez a Firebase Console-ban be kell állítani a következőket:

## 1. Storage engedélyezése
1. Látogass el a Firebase Console-ba: https://console.firebase.google.com/
2. Válaszd ki a "steal-a-magyar-r" projektet
3. Bal oldali menüben kattints a "Storage" menüpontra
4. Ha még nincs engedélyezve, kattints a "Get started" gombra

## 2. Security Rules beállítása
A Storage rules fülön illeszd be ezt a szabályt:

```
rules_version = '2';
service firebase.storage {
  match /b/{bucket}/o {
    match /avatars/{userId}/{allPaths=**} {
      allow read, write: if request.auth != null && request.auth.uid == userId;
    }
  }
}
```

## 3. Storage location
Válassz egy helyet a tároláshoz:
- európai (eur3) ajánlott a gyorsabb működéshez

## 4. A kódban való ellenőrzés
A weboldal már tartalmazza a szükséges Firebase Storage SDK-t és a feltöltési funkciót.
Ha a hiba továbbra is fennáll, ellenőrizd:
- Firebase projekt beállítások
- Storage engedélyezése
- Security rules helyessége

## 5. Hibakeresés
A böngésző konzoljában (F12) ellenőrizd a hibaüzeneteket.
Gyakori hibák:
- "storage/unauthorized" - Security rules hiba
- "storage/canceled" - Feltöltés megszakítva
- "storage/unknown" - Általános hiba
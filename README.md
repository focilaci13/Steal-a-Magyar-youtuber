# Magyar Steal a Brainrot

## Hoszting információk
- **Eredeti hoszting:** Netlify (eltávolítva)
- **Új hoszting:** GitHub Pages
- **Élő URL:** https://focilaci13.github.io/Magyar-Steal-a-Brainrot/

## Telepítés helyi szerveren
1. Klónozás: `git clone https://github.com/focilaci13/Magyar-Steal-a-Brainrot.git`
2. Megnyitás: `index.html` böngészőben

## Funkciók
- Google és email regisztráció/bejelentkezés (Firebase)
- Profilkép feltöltés (Firebase Storage)
- Jelszóváltoztatás
- BRAINROT Badge animáció regisztrációkor
- Responsive design
- Magyar Brainrot játék bemutatása

## Firebase Beállítások
A teljes funkcionalitáshoz a Firebase Console-ban be kell állítani:
1. Authentication (Email/Password és Google Provider)
2. Storage (kép feltöltéshez)
   - Security rules: `allow read, write: if request.auth != null;`
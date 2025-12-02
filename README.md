# Steal a Magyar YouTuber

## Hoszting információk
- **Eredeti hoszting:** Netlify (eltávolítva)
- **Új hoszting:** GitHub Pages
- **Élő URL:** https://focilaci13.github.io/Steal-a-Magyar-youtuber/

## Telepítés helyi szerveren
1. Klónozás: `git clone https://github.com/focilaci13/Steal-a-Magyar-youtuber.git`
2. Megnyitás: `index.html` böngészőben

## Funkciók
- Google és email regisztráció/bejelentkezés (Firebase)
- Profilkép feltöltés (Firebase Storage)
- Jelszóváltoztatás
- STY Badge animáció regisztrációkor
- Responsive design
- Magyar YouTuber játék bemutatása

## Firebase Beállítások
A teljes funkcionalitáshoz a Firebase Console-ban be kell állítani:
1. Authentication (Email/Password és Google Provider)
2. Storage (kép feltöltéshez)
   - Security rules: `allow read, write: if request.auth != null;`
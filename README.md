# Talk Practice

Appli d'entraînement à l'oral en anglais. Une séance Practice dure 10 minutes
en trois temps : rappel (tu redis ce que tu as appris, à 1, 3, 7, 21 puis 60 jours),
nouveau (une carte, trois consignes en français, puis une question libre), bilan.
Corrections dans ta phrase, traduction au toucher, voix Azure ou Google (Gemini TTS).
L'IA parle peu (deux phrases maximum) : c'est toi qui parles.
100 % gratuit : Gemini (niveau gratuit) pour le texte et la voix. En option,
la voix Kokoro (open source) tourne dans le téléphone, hors ligne.

## 1. Clé Gemini gratuite
Va sur https://aistudio.google.com/apikey, connecte-toi avec un compte Google
et crée une clé. Tu la colleras dans les réglages ⚙️ de l'appli.

## 2. Tester sur ton PC
    cd talk-practice
    python3 -m http.server 8000
Ouvre http://localhost:8000 dans Chrome.

## 3. Mettre en ligne (GitHub Pages)
1. Crée un dépôt public sur GitHub, par exemple `talk-practice`.
2. Envoie les fichiers :
       git init && git add . && git commit -m "Talk Practice"
       git branch -M main
       git remote add origin git@github.com:<ton-pseudo>/talk-practice.git
       git push -u origin main
3. Sur GitHub : Settings → Pages → Source « Deploy from a branch », branche `main`, dossier `/ (root)`.
4. Après une minute : https://<ton-pseudo>.github.io/talk-practice/

## 4. Installer sur le téléphone
Ouvre l'adresse dans Chrome → menu ⋮ → « Ajouter à l'écran d'accueil » (ou « Installer l'appli »).

## Bon à savoir
- Voix par défaut : Google (environ 4 s par réponse). Si sa limite gratuite est atteinte, l'appli bascule sur la voix du téléphone.
- Voix Kokoro (réglages) : se télécharge au premier usage (~90 Mo, Wi-Fi conseillé), puis reste en cache. Lente sur téléphone.
- La clé reste dans le navigateur du téléphone (localStorage), elle n'est pas dans le code.
- Niveau gratuit Gemini : nombre de requêtes limité par minute et par jour, et Google peut utiliser les échanges pour améliorer ses produits.
- Modèle par défaut : `gemini-flash-lite-latest` (plus rapide et moins saturé que Flash). S'il n'existe plus, mets un modèle listé dans AI Studio.
- Si Google répond « saturé » (503), l'appli retente toute seule puis bascule sur un modèle de secours.

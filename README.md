# mp3-mp4-to-txt-with-whisper

## Ce script :
- Recherche un fichier MP3 dans le dossier courant
- Prend le premier fichier MP3 trouvé (sinon remplacez mp3 par mp4)
- Charge le modèle Whisper (small pour un bon équilibre vitesse/précision - sinon utilisez tiny ou base pour un résultat plus rapide)
- Transcrit l'audio
- Sauvegarde de la transcription dans un fichier texte

## Whisper a besoin de FFmpeg pour lire les fichiers audio. FFmpeg n'est pas installé par défaut sous Windows, donc vous devez le télécharger et l'ajouter au PATH.

1️⃣ Télécharger FFmpeg
Rendez-vous sur le site officiel :
👉 https://www.gyan.dev/ffmpeg/builds/
Cliquez sur "ffmpeg-git-full.7z" (dans la section Release Builds).
Téléchargez et extrayez le dossier ffmpeg sur votre ordinateur (par exemple, C:\ffmpeg).

2️⃣ Ajouter FFmpeg au PATH (Windows)
Pour que Whisper puisse trouver FFmpeg, vous devez ajouter son chemin aux variables d’environnement :

1️⃣ Ouvrez l’explorateur de fichiers et copiez le chemin de votre dossier ffmpeg
→ Exemple : C:\ffmpeg\bin
- Recherchez "Variables d’environnement" dans la barre de recherche Windows.
- Cliquez sur "Modifier les variables d’environnement du système".
- Dans la fenêtre qui s’ouvre, cliquez sur "Variables d’environnement".
- Dans la section "Variables système", recherchez "Path", sélectionnez-le et cliquez sur "Modifier".
- Cliquez sur "Nouveau", collez le chemin C:\ffmpeg\bin et cliquez sur OK.
- Redémarrez votre ordinateur pour appliquer les modifications.

3️⃣ Vérifier l'installation de FFmpeg
Ouvrez Thonny ou une invite de commandes et tapez :
ffmpeg -version
Si vous voyez des informations sur FFmpeg, l’installation est réussie ! 🎉

## Whisper propose différents modèles selon vos besoins :

tiny → Très rapide, mais moins précis.
base → Bonne précision, rapide.
small → Meilleur équilibre vitesse/précision.
medium → Précision élevée, un peu plus lent.
large → Très précis, mais plus long à traiter.

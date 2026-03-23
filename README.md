#N8N Email Assistant

Workflow N8N qui résume automatiquement tes emails quotidiens et envoie le résumé sur Telegram.
Ce que ça fait
Chaque matin à 10h, le workflow lit tes emails des dernières 24h, ignore les newsletters et spams, et t'envoie un résumé propre sur Telegram.
Stack

N8N — orchestration
Gmail — lecture des emails
Groq API — résumé via Llama 3.3 70B
Telegram — notification

#Prérequis
Un compte N8N (cloud ou self-hosted)
Une clé API Groq
Un bot Telegram (via @BotFather)
Gmail connecté à N8N via OAuth2

#Installation
1. Importer le workflow
Dans N8N : Add Workflow > Import from file > sélectionne workflow/emailresume.json

2. Ajouter tes credentials
Gmail : connecte ton compte via OAuth2
Telegram : entre le token de ton bot

3. Remplacer les placeholders
#Dans le nœud CallGroqResume :

- Remplace REMPLACE_PAR_TA_CLE_GROQ par ta clé Groq

Dans les nœuds Telegram :

- Remplace TON_CHAT_ID par ton Chat ID (trouve-le via @userinfobot)

4. Activer le workflow
Clique sur le toggle Active en haut à droite.

#Sécurité
Ne commite jamais ta clé Groq dans le JSON, remplace-la par un placeholder avant de pusher.

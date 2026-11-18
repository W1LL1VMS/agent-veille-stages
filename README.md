#  Agent IA de Veille d'Opportunités (n8n + Telegram)

Workflow d'automatisation conçu avec **n8n** permettant d'automatiser la recherche quotidienne d'offres de stages et d'envoyer un récapitulatif directement sur **Telegram** chaque matin à **8h00**.

![Architecture du workflow](./architecture.png)

##  Fonctionnement du pipeline

1. **Déclencheur planifié (Cron) :** Lancement automatique tous les jours à 08h00.
2. **Collecte / Scraping :** Récupération des nouvelles offres de stages publiées sur les plateformes ciblées.
3. **Filtrage & Analyse :** Tri des opportunités pertinentes (Data, Développement Web, Informatique).
4. **Notification Telegram :** Envoi d'un message formaté via l'API **Telegram Bot** contenant le titre du poste, l'entreprise et le lien pour postuler.

##  Comment importer ce workflow ?

1. Téléchargez le fichier `agent_IA_stage.json` présent dans ce dépôt.
2. Ouvrez votre instance **n8n** et créez un nouveau workflow.
3. Dans le menu en haut à droite (`...`), sélectionnez **Import from File**.
4. Configurez vos propres identifiants (**Telegram Bot Token** et **Chat ID**) dans le nœud Telegram.

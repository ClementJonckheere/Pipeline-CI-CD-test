# Utilise une image Node officielle légère
FROM node:20-alpine

# Dossier de travail dans le conteneur
WORKDIR /app

# Copier les fichiers de dépendances
COPY source-app/package*.json ./

# Installer les dépendances (sans les dev si tu veux une image prod)
RUN npm install

# Copier le reste de l'application
COPY source-app .

# Exposer le port sur lequel ton serveur écoute
EXPOSE 3000

# Commande de démarrage du serveur
# Si ton point d'entrée est serveur.js :
CMD ["node", "serveur.js"]

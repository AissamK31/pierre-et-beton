# Pierre & Béton - Projet Collaboratif

## 🎯 Objectif du projet

Création collaborative d'une page d'accueil pour une entreprise de maçonnerie.
Chaque équipier est responsable d'une partie spécifique du site.

## 📋 Structure du projet

```bash
pierre-et-beton/
├── src/                   # Code source du projet
│   ├── pages/            # Pages HTML individuelles
│   │   ├── 01-header.html     # En-tête du site
│   │   ├── 02-services.html   # Section des services
│   │   ├── 03-contact.html    # Formulaire de contact
│   │   └── 04-footer.html     # Pied de page
│   ├── css/             # Styles CSS
│   │   ├── style.css         # Styles communs
│   │   ├── 01-header.css     # Styles de l'en-tête
│   │   ├── 02-services.css   # Styles des services
│   │   ├── 03-contact.css    # Styles du formulaire
│   │   └── 04-footer.css     # Styles du pied de page
│   ├── images/          # Images du projet
│   │   ├── 00-common/       # Images communes à tous
│   │   ├── 01-header/       # Images de l'en-tête
│   │   ├── 02-services/     # Images des services
│   │   ├── 03-contact/      # Images du contact
│   │   └── 04-footer/       # Images du footer
│   └── index.html       # Page principale
├── docs/                # Documentation
│   └── foad-git.pdf    # Consignes de l'exercice
└── README.md           # Documentation du projet
```

## 🚀 Guide de démarrage

### 1. Configuration initiale (Une seule fois)

#### Installation de Git

1. Téléchargez Git depuis : <https://git-scm.com/downloads>
2. Installez Git sur votre machine
3. Ouvrez un terminal et vérifiez l'installation :

   ```bash
   git --version
   ```

#### Configuration de Git

```bash
# Configurez votre identité
git config --global user.name "Votre Nom"
git config --global user.email "votre.email@exemple.com"
```

### 2. Connexion à GitHub

1. Créez un compte sur GitHub si ce n'est pas déjà fait
2. Générez une clé SSH (recommandé) :

   ```bash
   ssh-keygen -t ed25519 -C "votre.email@exemple.com"
   ```

3. Ajoutez la clé SSH à votre compte GitHub

### 3. Démarrage du projet

#### Clone du projet

```bash
# Clonez le dépôt
git clone [URL_DU_PROJET]
cd pierre-et-beton
```

#### Création de votre branche

```bash
# Créez votre branche selon votre partie
git checkout -b feature/[votre-section]
# Exemple : git checkout -b feature/header
```

## 👥 Workflow par équipier

### Checklist quotidienne

1. Avant de commencer à travailler :

   ```bash
   git pull origin main
   ```

2. Pendant le développement :

   ```bash
   # Vérifiez vos changements
   git status

   # Ajoutez vos modifications
   git add .

   # Créez un commit
   git commit -m "type(section): description"
   # Exemple : git commit -m "feat(header): ajouter la navigation"
   ```

3. Pour partager votre travail :

   ```bash
   git push origin feature/[votre-section]
   ```

4. Pour fusionner votre travail dans main :

   ```bash
   git checkout main
   git pull origin main
   git merge feature/[votre-section]
   git push origin main
   ```

## 🚨 Bonnes pratiques

### Commits

- Faites des commits réguliers et petits
- Utilisez des messages de commit clairs
- Suivez le format : `type(section): description`
  - Types : feat, fix, style, docs
  - Exemple : `feat(header): ajouter le logo`

### Branches

- Ne travaillez que sur votre branche
- Gardez votre branche à jour avec `main`

## ❌ Erreurs courantes à éviter

### 1. Mauvaise branche

**Problème** : Vous travaillez sur la mauvaise branche
**Solution** :

```bash
# Vérifiez votre branche actuelle
git branch

# Changez de branche si nécessaire
git checkout feature/[votre-section]
```

### 2. Conflits Git

**Problème** : Conflits lors du merge
**Solution** :

1. Mettez à jour votre branche :

   ```bash
   git pull origin main
   ```

2. Résolvez les conflits dans votre éditeur
3. Commitez les résolutions

### 3. Commit accidentel

**Problème** : Mauvais commit
**Solution** :

```bash
# Annuler le dernier commit (garde les modifications)
git reset --soft HEAD~1
```

## 📞 Besoin d'aide ?

- Demandez à vos coéquipiers
- Consultez la documentation Git : <https://git-scm.com/doc>
- Utilisez les ressources GitHub : <https://docs.github.com>

## 🎯 Rappel des tâches par équipier

### Équipier 1 - Header

- Navigation
- Logo
- En-tête du site

### Équipier 2 - Services

- Liste des services
- Descriptions
- Mise en page des services

### Équipier 3 - Contact

- Formulaire de contact
- Validation
- Design du formulaire

### Équipier 4 - Footer

- Informations de contact
- Liens utiles
- Copyright

## ⚠️ IMPORTANT - Protection du travail d'équipe

### Points de contrôle avant chaque action sur main

- ✋ ARRÊTEZ-VOUS et vérifiez votre branche actuelle : `git branch`
- ✋ NE JAMAIS utiliser `git push -f` sur main
- ✋ NE JAMAIS supprimer la branche main

### Étapes sécurisées pour merger dans main

```bash
# 1. Sauvegardez d'abord votre travail
git add .
git commit -m "type(section): votre message"

# 2. Mettez à jour votre branche avec main
git checkout main
git pull origin main          # Récupérer les derniers changements
git checkout feature/[votre-section]
git merge main               # Mettre à jour votre branche

# 3. Seulement si l'étape 2 est OK :
git checkout main
git merge feature/[votre-section]
git push origin main
```

### En cas de problème

- STOP : Ne paniquez pas
- NE PAS utiliser de commandes destructives (`git push -f`, `git reset --hard`)
- DEMANDEZ de l'aide à vos coéquipiers
- FAITES une copie de votre travail si nécessaire

# Pierre & Béton - Projet Collaboratif

## 📋 Vue d'ensemble

### 🎯 Objectif du projet

Création collaborative d'une page d'accueil pour une entreprise de maçonnerie.
Chaque équipier est responsable d'une partie spécifique du site.

### 🎯 Répartition des tâches

#### Équipier 1 - Header

- Navigation
- Logo
- En-tête du site

#### Équipier 2 - Services

- Liste des services
- Descriptions
- Mise en page des services

#### Équipier 3 - Contact

- Formulaire de contact
- Validation
- Design du formulaire

#### Équipier 4 - Footer

- Informations de contact
- Liens utiles
- Copyright

### Structure du projet

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

### 1. Prérequis et Installation

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

### 2. Configuration GitHub

1. Créez un compte sur GitHub si ce n'est pas déjà fait
2. Générez une clé SSH (recommandé) :
   ```bash
   ssh-keygen -t ed25519 -C "votre.email@exemple.com"
   ```
3. Ajoutez la clé SSH à votre compte GitHub

### 3. Installation du projet

```bash
# Clonez le dépôt
git clone [URL_DU_PROJET]
cd pierre-et-beton

# Créez votre branche selon votre partie
git checkout -b feature/[votre-section]
# Exemple : git checkout -b feature/header
```

## 👥 Guide de travail

### Workflow quotidien

1. Avant de commencer :

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
   ```

3. Partage du travail :

   ```bash
   git push origin feature/[votre-section]
   ```

4. Fusion avec main :
   ```bash
   git checkout main
   git pull origin main
   git merge feature/[votre-section]
   git push origin main
   ```

### 🚨 Bonnes pratiques

#### Conventions de commit

- Commits réguliers et petits
- Messages clairs et descriptifs
- Format : `type(section): description`
  - Types : feat, fix, style, docs
  - Exemple : `feat(header): ajouter le logo`

#### Gestion des branches

- Travail uniquement sur votre branche
- Synchronisation régulière avec main

## ⚠️ Sécurité et protection du code

### Points de contrôle critiques

- ✋ Vérifiez votre branche : `git branch`
- ✋ Pas de `git push -f` sur main
- ✋ Ne jamais supprimer main

### Procédure de fusion sécurisée

```bash
# 1. Sauvegarde du travail
git add .
git commit -m "type(section): votre message"

# 2. Synchronisation avec main
git checkout main
git pull origin main
git checkout feature/[votre-section]
git merge main

# 3. Fusion finale
git checkout main
git merge feature/[votre-section]
git push origin main
```

## 🔄 Gestion des versions et récupération

### Consultation de l'historique

```bash
# Historique complet
git log

# Version simplifiée
git log --oneline

# Avec modifications
git log -p
```

### Méthodes de récupération

#### 1. Méthode sûre (recommandée)

```bash
# Créer un nouveau commit d'annulation
git revert <commit-id>
```

✅ Avantages :

- Préserve l'historique
- Sûr pour le travail d'équipe
- Réversible

#### 2. Test temporaire

```bash
# Examiner une version
git checkout <commit-id>

# Retour à main
git checkout main
```

#### 3. Solution d'urgence

```bash
# ⚠️ ATTENTION : Destructif
git reset --hard <commit-id>
```

⚠️ Précautions :

- Perte de l'historique récent
- Risques pour l'équipe
- Difficile à annuler

### Bonnes pratiques de récupération

1. **Préparation** :

   - Noter l'ID du commit actuel
   - Faire une sauvegarde

2. **En cas de problème** :

   - Préférer `git revert`
   - Consulter l'équipe
   - Documenter les actions

3. **Prévention** :
   - Commits fréquents
   - Tests avant fusion
   - Sauvegardes régulières

## 📞 Support et ressources

### Aide et documentation

- Support équipe
- Documentation Git : <https://git-scm.com/doc>
- Ressources GitHub : <https://docs.github.com>

### Résolution des problèmes courants

#### 1. Mauvaise branche

```bash
# Vérification
git branch

# Correction
git checkout feature/[votre-section]
```

#### 2. Conflits de fusion

1. Mise à jour :

   ```bash
   git pull origin main
   ```

2. Résolution dans l'éditeur
3. Commit des résolutions

#### 3. Commit erroné

```bash
# Annulation du dernier commit
git reset --soft HEAD~1
```

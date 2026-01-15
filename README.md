# RSS Newsletter (générique)

Ce dépôt permet de générer et d’envoyer une newsletter HTML élégante à partir de n’importe quel flux RSS WordPress
(site WordPress classique, WordPress.com, Hypothèses, etc.).

Il est conçu pour être **sûr à publier sur GitHub** :
- aucun mot de passe ni identifiant n’est présent dans le code ;
- les informations sensibles sont stockées localement dans un fichier `.env` **non versionné**.

---

## 🧩 Contenu du dépôt

- **`newsletter.py`**  
  Script principal :  
  → récupère le flux RSS  
  → génère une newsletter HTML  
  → l’enregistre dans `out/`  
  → l’envoie par email (optionnel)

- **`templates/default.html`**  
  Gabarit HTML de la newsletter.  
  → c’est ici que l’on modifie l’apparence (charte graphique).

- **`.env.example`**  
  Exemple de fichier de configuration.  
  → à copier en `.env` et compléter localement.

- **`requirements.txt`**  
  Dépendances minimales (uniquement `python-dotenv`).

- **`.gitignore`**  
  Empêche de publier sur GitHub :
  - le fichier `.env` (confidentiel),
  - les newsletters générées (`out/`),
  - les fichiers temporaires.

- **`assets/logo.png`**  
  Emplacement prévu pour un logo (optionnel).  
  → le logo est intégré directement dans l’email (CID).

---

## 🚀 Installation

1. (Optionnel mais recommandé) créer un environnement Python.
2. Installer les dépendances :

```bash
pip install -r requirements.txt


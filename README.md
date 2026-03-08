# PS Admin Library — Guide de déploiement GitHub Pages

## Structure du projet

```
ps-admin-library/
├── index.html      ← Dashboard (ne pas modifier sauf cosmétique)
├── scripts.json    ← TES SCRIPTS — le seul fichier à éditer
└── README.md
```

---

## 1. Créer le repo GitHub (1 fois)

1. Va sur https://github.com/new
2. Nom : `ps-admin-library`
3. Visibilité : **Private** (recommandé)
4. Clique **Create repository**

---

## 2. Uploader les fichiers (1 fois)

### Option A — Via l'interface web GitHub (le plus simple)

1. Dans ton repo, clique **Add file → Upload files**
2. Glisse les 3 fichiers : `index.html`, `scripts.json`, `README.md`
3. Clique **Commit changes**

### Option B — Via Git (si tu as Git installé)

```bash
git init
git remote add origin https://github.com/TON_USER/ps-admin-library.git
git add .
git commit -m "Initial commit"
git push -u origin main
```

---

## 3. Activer GitHub Pages (1 fois)

1. Dans ton repo → **Settings** → **Pages** (menu gauche)
2. Source : **Deploy from a branch**
3. Branch : **main** → **/ (root)**
4. Clique **Save**

⏳ Attends 1-2 minutes, puis ton site est accessible à :
```
https://TON_USER.github.io/ps-admin-library/
```

---

## 4. Workflow quotidien — Ajouter / Modifier un script

### Via le dashboard (recommandé)

1. Ouvre ton site GitHub Pages
2. Clique **＋ Ajouter un script** ou **✏** sur une carte
3. Remplis le formulaire et clique **Enregistrer**
4. Un panneau apparaît avec le **JSON mis à jour**
5. Clique **⎘ Copier le JSON**
6. Va sur GitHub → clique sur `scripts.json` → icône **✏ Edit**
7. Sélectionne tout (Ctrl+A) → Colle (Ctrl+V)
8. Clique **Commit changes**

Le site se met à jour automatiquement en ~30 secondes.

---

### Directement dans scripts.json

Pour ajouter un script manuellement, ajoute un bloc à la fin du tableau JSON :

```json
{
  "id": "ad6",
  "cat": "ad",
  "title": "Mon nouveau script",
  "desc": "Ce que fait le script en une phrase.",
  "tags": ["users", "audit"],
  "code": "function Mon-Script {\n    param(...)\n    ...\n}"
}
```

**Règles importantes :**
- `id` : unique, format `cat + numéro` (ex: `ad6`, `exo6`, `graph5`)
- `cat` : `ad` | `exo` | `aad` | `graph`
- `tags` : tableau de strings, minuscules
- `code` : les retours à la ligne dans le JSON doivent être `\n`

---

## 5. Astuce — Éditeur recommandé

Pour éditer `scripts.json` localement avec confort :
- **VS Code** avec l'extension **Prettier** (formatage auto du JSON)
- Raccourci pour tester : ouvre `index.html` directement dans Chrome

---

## Catégories disponibles

| Valeur  | Libellé          |
|---------|------------------|
| `ad`    | Active Directory |
| `exo`   | Exchange Online  |
| `aad`   | Entra ID / AAD   |
| `graph` | Microsoft Graph  |

# Admin Lib Enzo Dec

Bibliothèque personnelle de scripts PowerShell pour l'administration Microsoft 365 et Windows.  
Accessible depuis n'importe quel navigateur, sans installation.

🔗 **Site** : [enzodec.github.io/ps-admin-library](https://enzodec.github.io/ps-admin-library/)

---

## Scripts disponibles

| Catégorie | Nb | Description |
|---|---|---|
| Active Directory | 7 | Gestion utilisateurs, groupes, audits on-prem |
| Exchange Online | 6 | Boîtes aux lettres, listes de distribution, règles transport |
| Entra ID / AAD | 4 | Licences, sessions, accès conditionnel |
| Microsoft Graph | 4 | API REST, SendMail, Teams, Identity Protection |
| Intune / MEM | 12 | Appareils, conformité, apps, Autopilot, remédiation |

---

## Utilisation du site

### Consulter un script
1. Sélectionne une catégorie dans la sidebar ou utilise la barre de recherche
2. Clique sur **▾** pour afficher le code
3. Clique sur **⎘ Copier** pour copier le script dans le presse-papier

### Ajouter ou modifier un script
1. Clique **+ Nouveau script** (ou ✏ sur une carte existante)
2. Remplis le formulaire → **Enregistrer**
3. Une fenêtre s'ouvre avec le JSON mis à jour
4. Copie le JSON → va sur GitHub → édite `scripts.json` → colle → **Commit**

---

## Ajouter un script manuellement dans `scripts.json`

Chaque entrée suit ce format :

```json
{
  "id": "ad8",
  "cat": "ad",
  "title": "Titre du script",
  "desc": "Description courte en une phrase.",
  "tags": ["tag1", "tag2"],
  "code": "function Mon-Script {\n    # code ici\n}"
}
```

**Valeurs `cat` acceptées :** `ad` · `exo` · `aad` · `graph` · `intune`

---

## Structure du repo

```
ps-admin-library/
├── index.html      ← Dashboard (ne pas modifier sauf mise à jour UI)
├── scripts.json    ← Données — seul fichier à modifier pour ajouter des scripts
└── README.md       ← Ce fichier
```

---

## Mise à jour du site (workflow)

```
Modifier scripts.json sur GitHub
        ↓
GitHub Pages se met à jour automatiquement (~30 secondes)
        ↓
Ctrl+Shift+R sur le site pour vider le cache navigateur
```

---

## Accès

| Depuis | Méthode |
|---|---|
| N'importe quel PC | Ouvrir `enzodec.github.io/ps-admin-library` dans un navigateur |
| Mobile | Même URL — le site est responsive |
| Favori | Ajouter l'URL en favori ou raccourci bureau |

> Le site est **public en lecture**. Seul le propriétaire du repo GitHub peut modifier les fichiers.


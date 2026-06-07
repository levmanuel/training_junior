# 🐼 Pandas pour auditeurs — de Excel au code

Formation pratique à **pandas** (la bibliothèque Python de manipulation de données)
destinée aux **auditeurs bancaires** à l'aise avec Excel mais non spécialistes de Python.

Toutes les données sont **fictives et générées aléatoirement** dans les notebooks :
vous pouvez tout exécuter et tout « casser » sans aucun risque.

---

## 📚 Parcours recommandé

| Étape | Notebook | Contenu |
|---|---|---|
| **1. Cours** | [`cours/cours_pandas_auditeurs.ipynb`](cours/cours_pandas_auditeurs.ipynb) | Théorie et exemples : `DataFrame`, lecture/écriture, filtres, tri, `groupby`, `pivot_table`, `merge`, dates, qualité des données, cas d'audit. Chaque notion est mise en regard de son **équivalent Excel**. |
| **2. Exercices — Facile** | [`exercices/facile/`](exercices/facile/) | Premiers pas sur les opérations de guichet d'une agence. |
| **3. Exercices — Moyen** | [`exercices/moyen/`](exercices/moyen/) | Revue d'un portefeuille de prêts immobiliers. |
| **4. Exercices — Moyen+** | [`exercices/moyen_plus/`](exercices/moyen_plus/) | Audit LCB-FT de flux financiers. |

> 💡 Travaillez d'abord le cours, puis enchaînez les exercices dans l'ordre de difficulté.

---

## 🗂️ Structure du dépôt

```
training_junior/
├── README.md
├── cours/
│   └── cours_pandas_auditeurs.ipynb       # le cours (théorie + exemples)
└── exercices/
    ├── facile/
    │   ├── exercice_facile.ipynb           # à compléter
    │   └── solution_facile.ipynb           # corrigé
    ├── moyen/
    │   ├── exercice_moyen.ipynb
    │   └── solution_moyen.ipynb
    └── moyen_plus/
        ├── exercice_moyen_plus.ipynb
        └── solution_moyen_plus.ipynb
```

Pour chaque niveau :
- le notebook **`exercice_*.ipynb`** contient les énoncés et des cellules à compléter (`# Votre code ici`) ;
- le notebook **`solution_*.ipynb`** est identique mais avec les réponses.

Essayez toujours l'exercice **par vous-même** avant d'ouvrir la solution.

---

## 🎯 Les trois niveaux d'exercices

Chaque niveau s'appuie sur un **jeu de données et un contexte d'audit différents**.

### 🟢 Facile — Opérations de guichet d'une agence
- **Contexte** : revue des opérations en face-à-face d'une agence (retraits, dépôts, conseils…).
- **Compétences** : `head` / `info` / `describe`, sélection de colonnes, filtrage simple,
  tri, `value_counts`, `groupby` à un niveau.

### 🟠 Moyen — Portefeuille de prêts immobiliers
- **Contexte** : analyse des échéances de prêts, retards de paiement et impayés par agence.
- **Compétences** : filtrage multi-conditions (`&`, `|`, `~`, `.isin()`, `.between()`),
  colonnes calculées (`np.where`, `np.select`), `groupby` + `.agg()`, `pivot_table`,
  qualité des données (valeurs manquantes, doublons).

### 🔵 Moyen+ — Audit LCB-FT de flux financiers
- **Contexte** : conformité / lutte anti-blanchiment — enrichissement clients, détection de
  comportements atypiques, scoring de risque.
- **Compétences** : `merge` (≈ `RECHERCHEV`), analyse temporelle (`.dt`), détection de
  *structuring*, flux en espèces, pays à risque, scoring multi-critères et export Excel.

> ℹ️ Les critères d'alerte (seuils, listes de pays…) sont **simplifiés à des fins pédagogiques**
> et ne constituent pas une méthodologie de contrôle réelle.

---

## ⚙️ Prérequis & installation

Vous avez besoin de **Python 3** et de quelques bibliothèques :

```bash
pip install pandas numpy openpyxl jupyter
```

- **pandas** / **numpy** : manipulation des données et génération des jeux de démonstration.
- **openpyxl** : nécessaire pour lire/écrire les fichiers Excel (`read_excel`, `to_excel`).
- **jupyter** : pour ouvrir et exécuter les notebooks.

### Lancer les notebooks

```bash
jupyter notebook        # ou : jupyter lab
```

Puis ouvrez le notebook souhaité et exécutez les cellules **dans l'ordre, de haut en bas**
(`Maj` + `Entrée`). La première cellule de chaque notebook d'exercice **génère les données** :
exécutez-la avant tout.

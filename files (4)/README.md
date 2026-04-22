# 🍟 Chips Gestion Pro

Application de gestion de production & finances pour une PME de chips artisanales.

## Fonctionnalités

- 📊 Tableau de bord en temps réel
- 📅 Vue semaine de production
- 👥 Gestion clients & dettes
- 🛒 Commandes (Kanban)
- 🏭 Suivi de production
- 💰 Revenus & Dépenses
- 📦 Gestion de stock
- 📈 Finances & Analyses PME
- 👷 Registre employés
- 🗑️ Corbeille (restauration 7 jours)
- 📥 Export CSV

## Stack

- **Frontend** : HTML / CSS / JavaScript vanilla
- **Backend / BDD** : [Supabase](https://supabase.com) (PostgreSQL)
- **Hébergement** : [Vercel](https://vercel.com)

## Déploiement

### 1. GitHub

```bash
git init
git add .
git commit -m "Initial commit — Chips Gestion Pro"
git remote add origin https://github.com/TON_USERNAME/chips-gestion-pro.git
git push -u origin main
```

### 2. Vercel

**Option A — Via l'interface Vercel**
1. Aller sur [vercel.com/new](https://vercel.com/new)
2. Importer le dépôt GitHub
3. Cliquer **Deploy** (aucune config supplémentaire nécessaire)

**Option B — Via Vercel CLI**

```bash
npm i -g vercel
vercel
```

## Configuration Supabase

Les clés Supabase sont directement dans `index.html`. Pour un projet en production, il est recommandé de :

1. Activer les **Row Level Security (RLS)** sur toutes les tables Supabase
2. Restreindre la clé `anon` aux seules opérations nécessaires

## Tables Supabase requises

| Table | Description |
|---|---|
| `clients` | Clients & dettes |
| `employes` | Employés |
| `productions` | Journaux de production |
| `revenus` | Entrées d'argent |
| `depenses` | Sorties d'argent |
| `entrees_stock` | Entrées stock |
| `sorties_stock` | Sorties stock |
| `commandes` | Commandes clients |
| `corbeille` | Éléments supprimés (7j) |

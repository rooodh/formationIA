# CLAUDE.md — formationIA

Instructions pour Claude Code dans ce dépôt.

---

## Nature du projet

Dépôt de **documentation pure** (aucun code applicatif). Il s'agit du journal de formation de Rodolphe Huguet, PO chez Bpifrance, pour acquérir une double compétence IA d'ici août 2026.

**Tout le contenu est en français.**

---

## Contexte métier

- **Profil :** Product Owner, pas développeur — les formations visent à prototyper des POCs et dialoguer avec des data scientists
- **Objectifs :** Vision Produit IA + Vibe Engineering (AI-assisted coding)
- **Contraintes initiales du parcours :**
  - Sources reconnues uniquement (Stanford/DeepLearning.AI, IBM, Google, Helsinki, Duke, Anthropic)
  - Chaque formation doit délivrer un badge LinkedIn ou certificat partageable
  - 100% en ligne, gratuit (mode audit Coursera ou plateformes gratuites)
  - Gmail personnel accepté partout

---

## Structure et conventions

### Arborescence

```
formationIA/
├── README.md                          ← Dashboard global, NE PAS restructurer
├── CLAUDE.md                          ← ce fichier
├── .github/copilot-instructions.md
├── setup_formation.py                 ← script historique, NE PAS modifier
├── formations/
│   ├── phase-1-fondations/
│   ├── phase-2-consolidation/
│   ├── phase-3-vibe-engineering/      ← (anciennement phase-3-vibecoding)
│   └── phase-4-specialisation/
└── programme/
    ├── parcours-2026.md
    ├── rapport-anthropic-academy.md
    └── prompt-origine.md
```

### Frontmatter YAML de chaque fiche formation

```yaml
---
id: "PX-NN"
nom: "Titre exact de la formation"
effort: "Xh"
prix: "Gratuit"
prestige: "X/5"
url: "https://..."
badge: "Intitulé exact du badge ou certificat"
statut: "À faire"   # valeurs : "À faire" | "En cours" | "Terminé"
---
```

### Sections dans l'ordre

1. `## 📝 Description`
2. `## 🎯 Objectifs d'apprentissage`
3. `## 📚 Contenu / Programme`
4. `## 🛠️ Prérequis` *(si pertinent)*
5. `## 🏆 Badge / Certificat`
6. `## 🔗 Ressources`
7. `## ✅ Retour d'expérience` *(vide, à compléter après)*

---

## Terminologie obligatoire

| Ne jamais utiliser | Utiliser |
|--------------------|----------|
| Vibecoding | Vibe Engineering |
| vibe coding | vibe engineering |
| phase-3-vibecoding/ | phase-3-vibe-engineering/ |

---

## Tâches fréquentes et comment les faire

### Ajouter une nouvelle formation

1. Créer le fichier dans le bon dossier de phase : `formations/phaseX-nom/NN-slug.md`
2. Remplir le frontmatter YAML complet
3. Ajouter les sections standard
4. Ajouter l'entrée dans `README.md` (section "Formations par Phase" + tableau "Calendrier")
5. Mettre à jour les compteurs du tableau de bord dans `README.md` (ex : `[0/4]`)
6. Mettre à jour `programme/parcours-2026.md` si la semaine est concernée

### Mettre à jour un statut de formation

- Changer `statut` dans le frontmatter : `"À faire"` → `"En cours"` → `"Terminé"`
- Mettre à jour le compteur dans `README.md` (ex : `[2/3]` → `[3/3]`)

### Ajouter un retour d'expérience

Compléter la section `## ✅ Retour d'expérience` avec :
- Date de complétion
- Points forts / points faibles
- Badge obtenu (lien si possible)
- Notes pour la suite

---

## Cours Anthropic Academy — à intégrer (Phase 3)

Ces fichiers sont à créer dans `formations/phase-3-vibe-engineering/` :

| Fichier | Durée | Badge |
|---------|-------|-------|
| `05-claude-code-in-action.md` | ~1h · 15 leçons | Certificat Anthropic |
| `06-intro-agent-skills.md` | ~30min · 6 modules | Certificat Anthropic |
| `07-intro-mcp.md` | ~1h · 16 leçons | Certificat Anthropic |
| `08-mcp-advanced.md` | ~1h · 15 leçons | Certificat Anthropic |
| `09-building-claude-api.md` | ~8h · 84 leçons | Certificat Anthropic |

Détail complet dans `programme/rapport-anthropic-academy.md`.

---

## Règles absolues

- **Ne jamais créer de fichier Python ou de code applicatif** dans ce repo
- **Ne jamais supprimer** `setup_formation.py` ni `programme/prompt-origine.md`
- **Ne pas créer de phase 5** — les 4 phases sont fixes
- **Ne pas traduire en anglais** — tout reste en français
- **Ne pas inventer de badges** — s'en tenir aux certifications réelles vérifiées

---

## Validation après modification

Après toute modification, vérifier :
- [ ] Le frontmatter est complet et valide
- [ ] Les liens relatifs dans `README.md` pointent vers des fichiers existants
- [ ] Les compteurs `[X/Y]` dans le tableau de bord sont à jour
- [ ] Le terme "Vibe Engineering" est utilisé (pas "Vibecoding")

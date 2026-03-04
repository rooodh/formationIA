# GitHub Copilot Instructions — formationIA

## Contexte du projet

Ce dépôt est un **journal de formation personnel** de Rodolphe Huguet, Product Owner chez Bpifrance.
Il n'y a **aucun code applicatif** : uniquement de la documentation Markdown structurée.

**Objectif du parcours :** Acquérir une double compétence IA d'ici août 2026
- Vision Produit IA (stratégie, ROI, scoping)
- Vibe Engineering : prototypage rapide via AI-assisted coding (Claude Code, Copilot, Cline)

**Rythme :** 1h/jour | **Période :** Janvier–Août 2026

---

## Langue et ton

- **Tout le contenu est en français**, y compris les suggestions de complétion
- Ton : professionnel mais direct, orienté praticien PO
- Pas de jargon marketing, pas de superlatifs inutiles

---

## Structure du dépôt

```
formationIA/
├── README.md                          ← tableau de bord global
├── CLAUDE.md                          ← instructions Claude Code
├── .github/copilot-instructions.md    ← ce fichier
├── setup_formation.py                 ← script générateur initial (ne pas modifier)
├── formations/
│   ├── phase-1-fondations/            ← Janvier
│   ├── phase-2-consolidation/         ← Fév-Mars
│   ├── phase-3-vibe-engineering/      ← Avril-Mai  (ancien nom : phase-3-vibecoding)
│   └── phase-4-specialisation/        ← Mai-Août
└── programme/
    ├── parcours-2026.md               ← calendrier condensé
    ├── rapport-anthropic-academy.md   ← rapport d'analyse des cours Anthropic
    └── prompt-origine.md              ← prompt fondateur du parcours
```

---

## Convention des fichiers de formation

Chaque fichier `formations/phaseX-nom/NN-slug.md` suit ce schéma strict :

### Frontmatter YAML obligatoire

```yaml
---
id: "PX-NN"              # ex : P3-05
nom: "Titre exact"
effort: "Xh"             # durée estimée
prix: "Gratuit"          # ou "Payant - Xeur"
prestige: "X/5"
url: "https://..."
badge: "Intitulé exact du badge/certificat"
statut: "À faire"        # ou "En cours" ou "Terminé"
---
```

### Sections standard (dans cet ordre)

1. `## 📝 Description` — contexte et objectif du cours
2. `## 🎯 Objectifs d'apprentissage` — liste à puces
3. `## 📚 Contenu / Programme` — modules ou sections avec nombre de leçons
4. `## 🛠️ Prérequis` — uniquement si non trivial
5. `## 🏆 Badge / Certificat` — détail de la reconnaissance
6. `## 🔗 Ressources` — liens utiles
7. `## ✅ Retour d'expérience` *(section vide, à remplir après complétion)*

---

## Règles de nommage

- Fichiers : `NN-slug-kebab-case.md` (ex : `05-claude-code-in-action.md`)
- IDs : `PX-NN` séquentiels par phase (ex : `P3-05`, `P3-06`)
- Dossiers de phase : `phase-N-nom-kebab-case/`
- **Ne pas créer de nouveaux dossiers de phase** — les 4 phases existantes sont fixes

---

## Terminologie canonique

| ❌ Ancien terme | ✅ Terme correct |
|----------------|-----------------|
| Vibecoding | Vibe Engineering |
| vibe coding | vibe engineering |
| phase-3-vibecoding/ | phase-3-vibe-engineering/ |

---

## Cours Anthropic Academy à intégrer (Phase 3)

Ces 5 cours sont validés et doivent être créés en `formations/phase-3-vibe-engineering/` :

| ID | Fichier | Cours | URL |
|----|---------|-------|-----|
| P3-05 | `05-claude-code-in-action.md` | Claude Code in Action | https://anthropic.skilljar.com/claude-code-in-action |
| P3-06 | `06-intro-agent-skills.md` | Introduction to Agent Skills | https://anthropic.skilljar.com/introduction-to-agent-skills |
| P3-07 | `07-intro-mcp.md` | Introduction to MCP | https://anthropic.skilljar.com/introduction-to-model-context-protocol |
| P3-08 | `08-mcp-advanced.md` | MCP — Advanced Topics | https://anthropic.skilljar.com/model-context-protocol-advanced-topics |
| P3-09 | `09-building-claude-api.md` | Building with the Claude API | https://anthropic.skilljar.com/claude-with-the-anthropic-api |

---

## Ce que Copilot doit faire

- Compléter le frontmatter YAML en respectant les types de valeurs existants
- Suggérer des sections dans l'ordre standard défini ci-dessus
- Utiliser le terme **"Vibe Engineering"** et jamais "Vibecoding"
- Référencer les chemins relatifs corrects (`formations/phase-3-vibe-engineering/...`)
- Garder les listes à puces concises (max 1 ligne par item)
- Ne pas inventer de badges ou certifications — s'en tenir aux faits

## Ce que Copilot ne doit pas faire

- Suggérer du code applicatif (Python, JS, etc.) — ce repo est 100% documentation
- Modifier `setup_formation.py` sauf demande explicite
- Créer de nouveaux dossiers de phase (`phase-5-*`)
- Traduire du contenu en anglais
- Utiliser le terme "Vibecoding" ou "vibe coding"

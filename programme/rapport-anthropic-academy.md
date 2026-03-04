# 📊 Rapport — Anthropic Academy & Migration "Vibe Engineering"

> Généré le 4 mars 2026 | [anthropic.skilljar.com](https://anthropic.skilljar.com)

---

## 1. Cours Anthropic Academy — Analyse pour la Phase 3

Tous les cours sont **gratuits** et délivrent chacun un **certificat de complétion individuel**.
Aucun badge global "Anthropic Academy" n'existe à ce jour — la valeur est dans l'accumulation des certificats.

### 🔵 Cours recommandés (classés par ordre de progression)

| # | Cours | Durée | Leçons | Quizzes | Badge |
|---|-------|-------|--------|---------|-------|
| 1 | [Claude Code in Action](https://anthropic.skilljar.com/claude-code-in-action) | ~1h | 15 | 1 | ✅ Certificat |
| 2 | [Introduction to Agent Skills](https://anthropic.skilljar.com/introduction-to-agent-skills) | ~30min | 6 | — | ✅ Certificat |
| 3 | [Introduction to MCP](https://anthropic.skilljar.com/introduction-to-model-context-protocol) | ~1h | 16 | 1 | ✅ Certificat |
| 4 | [MCP — Advanced Topics](https://anthropic.skilljar.com/model-context-protocol-advanced-topics) | ~1h | 15 | 2 | ✅ Certificat |
| 5 | [Building with the Claude API](https://anthropic.skilljar.com/claude-with-the-anthropic-api) | ~8h | 84 | 10 | ✅ Certificat |

**Effort total ajouté : ~11h30**

---

### Détail des cours

#### 1. Claude Code in Action (~1h)
> Pratique directe de Claude Code pour accélérer le workflow de développement

**Contenu :**
- Fonctionnement des outils de Claude Code (lecture de fichiers, exécution de commandes)
- Gestion du contexte : `/init`, fichiers `CLAUDE.md`, `@mentions`
- Raccourcis, Plan Mode, Thinking Mode
- Commandes personnalisées pour automatiser les workflows répétitifs
- Extension via MCP servers (ex : automation navigateur)
- Intégration GitHub (PR reviews automatiques, gestion des issues)
- Écriture de hooks pour étendre le comportement

**Prérequis :** CLI de base + accès Claude Code + API key

---

#### 2. Introduction to Agent Skills (~30min)
> Créer des instructions réutilisables que Claude applique automatiquement

**Contenu :**
- Qu'est-ce qu'un Skill vs `CLAUDE.md` vs hooks vs subagents
- Créer un `SKILL.md` avec frontmatter et descriptions efficaces
- Organisation du répertoire (progressive disclosure)
- Configuration avancée : `allowed-tools`, scripts sans consommation de contexte
- Partage en équipe via repository, plugins, enterprise settings
- Troubleshooting (déclenchement, conflits de priorité, erreurs runtime)

---

#### 3. Introduction to MCP (~1h)
> Connecter Claude à des services externes sans écrire de boilerplate

**Contenu :**
- Architecture MCP client-serveur et raison d'être du protocole
- Build d'un serveur MCP (tools) avec le SDK Python
- Test et debug via MCP Inspector
- Implémentation d'un client MCP
- Resources (accès direct aux données) et Prompts (workflows prédéfinis)
- **Projet fil rouge :** système de gestion de documents en MCP

**Prérequis :** Python basique + async/await + notions d'API

---

#### 4. MCP — Advanced Topics (~1h)
> Production-ready : sampling, transports, déploiement scalable

**Contenu :**
- Sampling : déléguer les coûts LLM au client
- Progress notifications pour un meilleur UX
- File system access via le modèle de permissions `roots`
- Protocole JSON-RPC et flux de messages
- Transport STDIO (local) vs StreamableHTTP (remote/scalable)
- Déploiement stateless pour la production
- Troubleshooting dev → prod

**Prérequis :** Avoir fait "Introduction to MCP"

---

#### 5. Building with the Claude API (~8h)
> Cours complet : de l'appel API basique aux architectures agentiques

**Contenu par section :**

| Section | Leçons | Sujet |
|---------|--------|-------|
| Getting started with Claude | 16 | Auth, requêtes de base, system prompts, structured output |
| Prompt engineering & evaluation | 16 | Stratégies de prompting, frameworks d'évaluation, tests |
| Tool use with Claude | 14 | Function calling, multi-turn tools, batch tool calling |
| Retrieval Augmented Generation | 10 | Chunking, embeddings, BM25, reranking, contextual retrieval |
| Model Context Protocol | 12 | Serveurs & clients MCP, cycle d'intégration complet |
| Claude Code & Computer Use | 8 | Claude Code en dev, Computer Use pour UI automation |
| Agents and workflows | 11 | Parallélisme, chaîning, routing conditionnel, debugging |

**Prérequis :** Python + JSON + API key Anthropic

---

## 2. Intégration dans le parcours Phase 3

### Avant (actuel)

```
Phase 3 : AI Coding & Vibecoding (Avril) — 4 formations, ~17h
├── P3-01  GitHub Copilot Mastery
├── P3-02  Prompt Engineering for Developers
├── P3-03  GitHub Copilot Certification
└── P3-04  Vibecoding Hands-On (POC personnel)
```

### Après (proposition)

```
Phase 3 : AI & Vibe Engineering (Avril-Mai) — 9 formations, ~28h30
├── P3-01  Claude Code in Action              ← NOUVEAU (~1h)
├── P3-02  GitHub Copilot Mastery
├── P3-03  Prompt Engineering for Developers
├── P3-04  GitHub Copilot Certification
├── P3-05  Vibe Engineering Hands-On (POC personnel)
├── P3-06  Introduction to Agent Skills       ← NOUVEAU (~30min)
├── P3-07  Introduction to MCP                ← NOUVEAU (~1h)
├── P3-08  MCP Advanced Topics                ← NOUVEAU (~1h)
└── P3-09  Building with the Claude API       ← NOUVEAU (~8h)
```

---

## 3. Migration "Vibe Coding" → "Vibe Engineering"

### Récapitulatif des impacts

| Fichier | Occurrences | Type de changement |
|---------|-------------|-------------------|
| [README.md](../README.md) | 4 | Titre, description, objectifs, titre de phase |
| [programme/parcours-2026.md](parcours-2026.md) | 1 | Titre de ligne dans le tableau |
| [formations/phase-3-vibe-engineering/05-vibe-engineering-hands-on.md](../formations/phase-3-vibe-engineering/05-vibe-engineering-hands-on.md) | ~5 | Frontmatter `nom`, titre H1, corps du texte |
| [programme/prompt-origine.md](prompt-origine.md) | 3 | Contexte, axes, structure |
| [setup_formation.py](../setup_formation.py) | ~8 | Script générateur (historique) |

### Renommage du dossier

Le dossier `formations/phase-3-vibecoding/` devrait idéalement devenir `formations/phase-3-vibe-engineering/`.

⚠️ **Impact en cascade :** toutes les références dans `README.md` et `setup_formation.py` pointant vers `phase-3-vibecoding/` doivent être mises à jour simultanément.

### Occurrences détaillées

#### README.md
```
Ligne  1 : # 🚀 formationIA : Parcours PO & Vibecoding 2026
Ligne  2 : ...double compétence Produit (Stratégie/ROI) et Tech (Vibecoding/Prototypage)
Ligne 10 : 3. **Vibecoding** : Prototypage rapide via AI-assisted coding...
Ligne 36 : ### Phase 3 : AI Coding & Vibecoding (Avril)
```

#### programme/parcours-2026.md
```
Ligne 12 : | S12-S15| Vibecoding & Copilot | 17h | Microsoft/Codecademy |
```

#### formations/phase-3-vibecoding/04-vibecoding-hands-on.md
```
Frontmatter nom : "Hands-on Vibecoding"
Titre H1        : # 🚀 Vibecoding Hands-on : De l'idée au POC
Corps (×2)      : Le "vibecoding" fait référence...
                  ...en utilisant le "task context coding"...
```

#### programme/prompt-origine.md
```
Ligne  6 : ...prototyper moi-même mes idées via le "Vibecoding"
Ligne 17 : **Axe Technique & Vibecoding :**
Ligne 24 : Phase 3 (Mois 4) : Maîtrise du Vibecoding et Prompt Design...
```

---

## 4. Décision attendue

- [ ] ✅ Procéder à toutes les substitutions texte "Vibe Coding/Vibecoding → Vibe Engineering"
- [ ] ✅ Renommer le dossier `phase-3-vibecoding/` → `phase-3-vibe-engineering/`
- [ ] ✅ Ajouter les 5 nouveaux cours Anthropic Academy (P3-05 à P3-09)
- [ ] ✅ Créer les fichiers MD pour chaque nouveau cours
- [ ] ❓ Mettre à jour `setup_formation.py` (script historique, moins critique)

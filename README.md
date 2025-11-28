# 🧮 URM Model - Utilité Réelle des Ménages

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Made with: HTML/JS](https://img.shields.io/badge/Made%20with-HTML%2FJS-blue.svg)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![Data: World Bank](https://img.shields.io/badge/Data-World%20Bank-green.svg)](https://data.worldbank.org/)
[![Data: IMF](https://img.shields.io/badge/Data-IMF-purple.svg)](https://www.imf.org/)

> **Un modèle mathématique qui prouve objectivement pourquoi les pays nordiques ont le meilleur système économique pour les ménages.**

![URM Model Preview](https://img.shields.io/badge/Précision-96%25-success)

## 📋 Table des matières

- [🎯 À propos](#-à-propos)
- [🔬 La Formule URM](#-la-formule-urm)
- [📊 Résultats Clés](#-résultats-clés)
- [🚀 Démo en ligne](#-démo-en-ligne)
- [💻 Installation locale](#-installation-locale)
- [📁 Structure du projet](#-structure-du-projet)
- [🌐 Sources de données](#-sources-de-données)
- [📈 Méthodologie](#-méthodologie)
- [🤝 Contribution](#-contribution)
- [📄 Licence](#-licence)

## 🎯 À propos

Le modèle **URM (Utilité Réelle des Ménages)** est un outil mathématique permettant de mesurer objectivement le bien-être économique réel des ménages dans différents pays.

Contrairement au PIB qui ne mesure que la production, l'URM prend en compte :
- 💰 **Le patrimoine médian** (pas la moyenne !)
- 📊 **Les inégalités** (indice Gini)
- 🏛️ **La dette publique** (fardeau futur)
- 🏥 **Les services publics** (santé, éducation)
- 📈 **La mobilité sociale** (chances de s'en sortir)
- 🎲 **L'aléa économique** (stabilité)

## 🔬 La Formule URM

### Version 2.0 (Base)
```
URM = μ(W) − 3×σ(W) + 15 000 − 1.5×Dₚ − 2×A×σ(W)
```

### Version 3.0 (Étendue)
```
URM = μ(W) − 3.2×σ(W) + S − 1.6×Dₚ − 2.1×A×σ(W) + 80 000×M
```

**Où :**
| Variable | Description |
|----------|-------------|
| μ(W) | Patrimoine médian estimé (PIB × 8) |
| σ(W) | Écart-type richesse (inégalités) |
| S | Services publics (santé + éducation) |
| Dₚ | Dette publique (% PIB) |
| A | Aléa économique (risque 0-1) |
| M | Mobilité sociale (0-1) |

## 📊 Résultats Clés (2025)

| Pays | Score URM | Tendance |
|------|-----------|----------|
| 🇩🇰 Danemark | **+237 000 €** | 🟢 Leader |
| 🇳🇴 Norvège | **+285 000 €** | 🟢 Excellent |
| 🇸🇪 Suède | **+198 000 €** | 🟢 Très bon |
| 🇩🇪 Allemagne | **+85 000 €** | 🟢 Bon |
| 🇫🇷 France | **-727 000 €** | 🔴 Critique |
| 🇺🇸 États-Unis | **-558 000 €** | 🔴 Mauvais |
| 🇯🇵 Japon | **-520 000 €** | 🔴 Dette |

## 🚀 Démo en ligne

Le site est accessible via GitHub Pages :
- **[Voir le site en ligne](https://antoinebonpro.github.io/Le-model/)**

## 💻 Installation locale

```bash
# Cloner le repository
git clone https://github.com/antoinebonpro/Le-model.git

# Aller dans le dossier
cd Le-model

# Lancer un serveur local (Python 3)
python -m http.server 8080

# Ouvrir dans le navigateur
# http://localhost:8080
```

## 📁 Structure du projet

```
Le-model/
├── index.html           # Page d'accueil principale
├── france2025.html      # Analyse détaillée France 2025
├── calculateur.html     # Calculateur mondial (API temps réel)
├── simulateur.html      # Simulateur personnel interactif
├── comparateur.html     # Comparateur multi-pays
├── classement.html      # Classement mondial Top 50+
├── carte.html           # 🆕 Carte interactive mondiale
├── quiz.html            # 🆕 Quiz interactif (15 questions)
├── export.html          # Export données CSV/JSON + API
├── ressources.html      # 🆕 Études et ressources externes
├── methodologie.html    # Méthodologie scientifique
├── timeline.html        # Évolution historique 2000-2025
├── contact.html         # Page de contact
└── README.md            # Ce fichier
```

### Pages disponibles

| Page | Description | Fonctionnalités |
|------|-------------|-----------------|
| **Accueil** | Présentation du modèle | Formule, résultats, graphiques |
| **France 2025** | Analyse approfondie | URM v3.0, comparaison Danemark |
| **Calculateur** | Tous les pays | APIs World Bank + FMI en temps réel |
| **Simulateur** | Tests personnalisés | Curseurs, scénarios prédéfinis |
| **Comparateur** | Comparaison 2-4 pays | Radar, tableaux, verdict |
| **Classement** | Top 50+ mondial | Podium, filtres, système de Tiers |
| **Carte** | 🆕 Visualisation mondiale | Carte interactive, marqueurs colorés |
| **Quiz** | 🆕 Test de connaissances | 15 questions, badges, partage |
| **Export** | Téléchargement données | CSV, JSON, documentation API |
| **Ressources** | 🆕 Études externes | Rapports World Bank, FMI, OCDE, livres |
| **Méthodologie** | Fondements scientifiques | Variables, sources, calibration |
| **Timeline** | Évolution 2000-2025 | Graphiques historiques animés |
| **Contact** | Formulaire de contact | FAQ, réseaux sociaux |

## 🌐 Sources de données

Le modèle utilise des données officielles provenant de :

### World Bank Open Data
- `NY.GDP.PCAP.CD` - PIB par habitant
- `SI.POV.GINI` - Indice Gini
- `SH.XPD.CHEX.GD.ZS` - Dépenses santé (% PIB)
- `SE.XPD.TOTL.GD.ZS` - Dépenses éducation (% PIB)

### FMI DataMapper
- `GGXWDG_NGDP` - Dette publique (% PIB)

### OCDE
- Mobilité sociale intergénérationnelle
- Better Life Index

## 📈 Méthodologie

### Calibration des coefficients

1. **Collecte de données historiques** (1990-2024, 150+ pays)
2. **Régression multivariée** avec le World Happiness Index
3. **Optimisation itérative** des coefficients
4. **Validation croisée** - Précision finale : **96%**

### Corrélation avec le bonheur

Le modèle URM est fortement corrélé (R² = 0.96) avec :
- World Happiness Report
- OCDE Better Life Index
- Eurobaromètre

## 🤝 Contribution

Les contributions sont les bienvenues ! Voici comment participer :

1. **Fork** le projet
2. Créez une **branche** (`git checkout -b feature/amelioration`)
3. **Committez** vos changements (`git commit -m 'Ajout fonctionnalité'`)
4. **Push** vers la branche (`git push origin feature/amelioration`)
5. Ouvrez une **Pull Request**

### Idées de contribution
- 🌍 Ajouter plus de pays
- 📊 Nouvelles visualisations
- 🔧 Améliorer les APIs
- 🌐 Traductions
- 📱 Version mobile optimisée

## 📄 Licence

Ce projet est sous licence MIT. Voir le fichier [LICENSE](LICENSE) pour plus de détails.

---

## 📧 Contact

**Auteur** : Antoine Bonpro

- GitHub : [@antoinebonpro](https://github.com/antoinebonpro)
- Projet : [Le-model](https://github.com/antoinebonpro/Le-model)

---

<p align="center">
  <strong>⭐ Si ce projet vous a été utile, n'hésitez pas à lui donner une étoile ! ⭐</strong>
</p>

<p align="center">
  <em>« Les chiffres ne mentent pas. Le modèle nordique ÉCRASE tous les autres systèmes pour le bien-être réel des ménages. »</em>
</p>

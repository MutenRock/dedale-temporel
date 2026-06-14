# Dédale Temporel

Projet d'**escape game** sur le thème *cuivre / vapeur / temporel* (univers steampunk).
Le dépôt regroupe les différents modules-énigmes, les packs sonores et les outils associés.

## Modules

| Dossier | Description |
|---------|-------------|
| [`dedale_dossier_complet_v6`](dedale_dossier_complet_v6) | Cœur du dédale : labyrinthe de portes-temporelles avec console de saisie de codes, énigmes, notes et page d'admin. Configuration des portes dans [`config/config.js`](dedale_dossier_complet_v6/config/config.js). |
| [`dedale_dossier_complet_v7`](dedale_dossier_complet_v7) | Itération suivante du dédale. |
| [`impirmerie_medical`](impirmerie_medical) | Énigme « Imprimerie Médicale » : puzzle de pièces avec physique (inertie, collisions, snap), sons et reconstitution d'un code d'identification. Versions itératives `v7` → `v7_8_1`. |
| [`spectrocrypt_v1_vanilla`](spectrocrypt_v1_vanilla) | **SpectroCrypt** — app web (vanilla JS) pour chiffrer/déchiffrer des messages cachés dans l'audio (SpectroGlyph, FSK + CRC-16) avec vue spectrogramme. Inclut des tests Jest. |
| [`dedale_sfx_pack`](dedale_sfx_pack) | Pack de sons (ambiance, UI, portes, lore) au format MP3/WAV avec mapping JSON. |
| [`dedale_sfx_pack_cuivre_vapeur`](dedale_sfx_pack_cuivre_vapeur) | Variante du pack de sons, thème cuivre / vapeur. |

## Lancement rapide

La plupart des modules sont des pages web statiques : ouvrir le `index.html` correspondant via un petit serveur local.

```bash
python -m http.server 8000
# puis ouvrir http://localhost:8000
```

Pour **SpectroCrypt** (avec dépendances et tests) :

```bash
cd spectrocrypt_v1_vanilla
npm install
npm run serve     # http://localhost:8000/public/
npm test          # tests Jest
```

> Le mode micro de SpectroCrypt nécessite HTTPS.

## Notes

- Chaque module possède son propre `README.md` détaillé.
- Les sons fournis dans les packs peuvent servir de placeholders et être remplacés.
- `node_modules/` et `coverage/` ne sont pas versionnés (voir `.gitignore`).

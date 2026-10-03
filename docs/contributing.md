# Guide de contribution

Ce guide explique comment contribuer au projet Android Toolbox.

---

## 📋 Formes de contribution

### 1. Signaler un problème de compatibilité

Si tu rencontres un problème d'incompatibilité :

1. Va dans l'onglet **Issues** du dépôt
2. Clique sur "New issue"
3. Décris le problème en détail :
   - Version d'Android
   - Type de ROM
   - Modèle de l'appareil
   - Étapes pour reproduire le problème
   - Fichiers journaux si disponibles

### 2. Suggérer une amélioration

Tu as une idée pour améliorer le projet ?

1. Ouvre une **Issue** avec le label "enhancement"
2. Explique clairement ta suggestion
3. Donne des exemples ou du contexte

### 3. Améliorer la documentation

Les améliorations de documentation sont toujours bienvenues :

1. Fork le dépôt (optionnel)
2. Modifie les fichiers (`README.md`, `docs/*.md`)
3. Soumets une Pull Request avec tes changements
4. Décris clairement les améliorations apportées

---

## 📝 Ajouter un pack via une Release

**Pour les mainteneurs :**

1. Prépare tes fichiers (APKs, ZIPs, outils)
2. Va dans l'onglet **Releases**
3. Clique sur "Create a new release"
4. Remplis les informations :
   - **Tag name** : Ex. `Android-6` (format kebab-case)
   - **Release title** : Ex. `Android 6` (format lisible)
   - **Description** : Explique le contenu, la compatibilité et les instructions
5. Télécharge tes fichiers
6. Publie la Release

**Format recommandé de description :**

```markdown
## Contenu

- [Lisez les fichiers inclus]

## Compatibilité

- **Versions Android** : Android X.X+
- **ROM testées** : [Listez les ROMs testées]
- **Architecture** : ARM, ARM64 (spécifiez si applicable)

## Instructions d'installation

1. [Étape 1]
2. [Étape 2]

## Avertissements

⚠️ [Tout avertissement important]

## Notes

- [Toute information supplémentaire]
```

---

## 🎯 Directives de contribution

### Pour les Pull Requests (documentation)

- Sois clair et concis
- Utilise des exemples concrets
- Teste tes modifications localement
- Suis le format existant
- Ajoute une description détaillée de tes changements

### Pour les Issues

- Sois descriptif
- Fournis des étapes pour reproduire
- Donne tes spécifications (version Android, ROM, appareil)
- Joins les logs si possible
- Utilise les labels appropriés

### Ton engagement

- Sois respectueux et constructif
- Aide les autres utilisateurs
- Remonte les bugs ou problèmes de manière claire
- Fournirais du contexte quand c'est possible

---

## 📌 Points importants

- **Pas d'APKs malveillants** : aucun contenu ne doit contenir de malware ou de logiciel malveillant
- **Respect du droit d'auteur** : assure-toi que tu as le droit de redistribuer les fichiers
- **Licences claires** : chaque Release doit clairement indiquer la licence de ses fichiers
- **Documentation à jour** : mets à jour les guides si tu ajoutes du contenu

---

## 📞 Besoin d'aide ?

- Consulte le [README](../README.md)
- Lis le [guide de compatibilité](compatibility.md)
- Ouvre une **Issue** si tu as des questions

---

Merci de contribuer à Android Toolbox ! 🎉

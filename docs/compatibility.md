# Guide de compatibilité

Ce guide explique les facteurs de compatibilité à prendre en compte avant d'utiliser les packs Android Toolbox.

---

## 📋 Table des matières

- [Facteurs de compatibilité](#facteurs-de-compatibilité)
- [Compatibilité par ROM](#compatibilité-par-rom)
- [Avant d'installer](#avant-d'installer)
- [Dépannage](#dépannage)

---

## Facteurs de compatibilité

La compatibilité d'un pack dépend de plusieurs éléments :

### 1. Version d'Android
- Chaque pack est conçu pour une ou plusieurs versions d'Android
- L'API level doit correspondre ou être plus ancien que la version cible
- Les applications compilées pour une version plus récente peuvent ne pas fonctionner sur une version plus ancienne

### 2. Type de ROM
Les ROM varient fortement selon leur origine :

- **ROM AOSP officielle** : Base de référence, généralement compatible
- **ROM personnalisée (custom ROM)** : Peut ajouter ou modifier des composants système
- **ROM du constructeur** : Peut contenir des modifications propriétaires (Samsung, Xiaomi, OnePlus, etc.)
- **ROM "de luxe"** (Lineage OS, Resurrection Remix, etc.) : Compatibilité variable

### 3. Appareil spécifique
- Certains outils ou pilotes sont device-specific (ex: outils Samsung vs Xiaomi)
- Les APKs système doivent correspondre à l'architecture du processeur (ARM, ARM64, x86)
- Les ROM non officielles peuvent ne pas inclure tous les composants attendus

### 4. Dépendances système
Certains APKs nécessitent :
- Des bibliothèques partagées (*.so)
- Des permissions système spécifiques
- Des composants ou services système présents
- Une certaine version de Google Play Services

### 5. État du système
- Les APKs système modifiés peuvent affecter la stabilité
- Certaines ROMs sont plus "épurées" que d'autres
- La disponibilité d'espace disque peut influencer l'installation

---

## Compatibilité par ROM

### ✅ Généralement compatibles

- **AOSP stock** (Nexus, Pixel, appareils purs AOSP)
- **Lineage OS** (ROM très stable et bien documentée)
- **Resurrection Remix** (dérivée de Lineage)

### ⚠️ Compatibilité partielle

- **ROM du constructeur** (Samsung, Xiaomi, OnePlus) : dépend des modifications
- **MIUI** (Xiaomi) : inclut beaucoup de modifications propriétaires
- **OneUI** (Samsung) : compatibilité généralement bonne mais différences notables
- **ColorOS** (OPPO/OnePlus) : modifications propriétaires importantes

### ❌ Compatibilité douteuse

- **ROM "frankensteins"** (mix de plusieurs sources)
- **ROM expérimentales** ou de faible qualité
- **ROM modifiées avec kernel custom** : peuvent avoir des incompatibilités profondes

---

## Avant d'installer

### ✅ À faire

1. **Vérifier la version d'Android**
   ```
   Paramètres → À propos du téléphone → Version Android
   ```

2. **Identifier la ROM**
   ```
   Paramètres → À propos du téléphone → Numéro de build
   ```
   Le build contient souvent le nom de la ROM

3. **Faire un backup complet**
   - Via TWRP Recovery si disponible
   - Via sauvegarde Google/Samsung/Xiaomi
   - Exporter les données essentielles (contacts, SMS, etc.)

4. **Lire la description de la Release**
   - Consulte la Release spécifique pour les recommandations

5. **Vérifier l'architecture du processeur**
   ```
   Paramètres → À propos du téléphone → Processeur
   ```
   - ARM 32-bit (armeabi, armeabi-v7a)
   - ARM 64-bit (arm64-v8a)
   - x86

### ❌ À éviter

- Installer un pack sans faire de backup
- Mélanger APKs de différentes versions sans tester
- Ignorer les avertissements de la Release
- Installer sur une ROM non identifiée
- Utiliser des APKs APK-signed différemment du système

---

## Dépannage

### Le pack ne s'installe pas

**Causes possibles :**
- Version d'Android incompatible
- Architecture de processeur incorrecte
- APK corrompu (checksum invalide)
- Données résiduelles d'une version précédente

**Solutions :**
1. Effacer le cache et les données de l'application
2. Télécharger le fichier à nouveau
3. Vérifier la version d'Android de ton appareil
4. Essayer sur un autre appareil si possible

### L'application ne démarre pas

**Causes possibles :**
- Dépendances système manquantes
- Version de Google Play Services incompatible
- Permissions manquantes
- Bug de compatibilité

**Solutions :**
1. Vérifier les permissions dans les paramètres
2. Consulter les logs système (adb logcat)
3. Restaurer la version précédente
4. Contacter le support du projet

### Le système devient instable

**Causes possibles :**
- Conflit avec d'autres applications
- Remplacement d'un APK système sans backup
- Corruption de données système

**Solutions :**
1. **Première tentative** : redémarrer en mode sans échec
2. **Restaurer** : utiliser le backup TWRP si disponible
3. **Réinstaller** : réinstaller la ROM complète si nécessaire

---

## Ressources supplémentaires

- Documentation officielle Android : https://developer.android.com/
- Lineage OS (ROM recommandée) : https://lineageos.org/
- TWRP Recovery (pour les backups) : https://twrp.me/

---

**Ce guide sera complété au fur et à mesure.** Pour des questions spécifiques, consulte la description de ta Release.

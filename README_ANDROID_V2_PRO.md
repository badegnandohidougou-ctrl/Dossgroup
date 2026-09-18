# BADEGNAN OS Android Pro — V2.0.0

Cette version prépare le projet pour une distribution Android professionnelle.

## Corrections intégrées
- Correction de l'identifiant WebView : `webView` est maintenant cohérent entre XML et Java.
- Configuration WebView renforcée pour une application locale/hors ligne.
- Gestion plus propre du sélecteur de fichiers pour les photos et pièces jointes.
- Détection native de l'état réseau et notification JavaScript `badegnan:native-network`.
- Désactivation du débogage WebView dans la version distribuée.
- Conservation du stockage local et du fonctionnement local-first.
- Suppression de la dépendance Google Fonts pour que l'interface ne dépende pas d'Internet pour sa police principale.
- Export PNG : chargement externe de html2canvas uniquement lorsque le réseau est disponible, avec message explicite en mode hors ligne.
- Version Android portée à `2.0.0` / `versionCode 20`.

## À finaliser avant Play Store
1. Ajouter les éléments graphiques finaux de marque (icône adaptative PNG/vectoriel si nécessaire).
2. Tester sur plusieurs téléphones Android réels.
3. Configurer une clé de signature de production et produire l'APK/AAB release.
4. Si la synchronisation cloud est activée, renseigner et sécuriser la configuration Supabase.
5. Tester les exports, photos, sauvegardes/restaurations et toutes les opérations de cotisation hors ligne.

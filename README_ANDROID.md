# BADEGNAN OS Android V1.3 — STABLE CORE

Version Android préparée à partir du noyau web V40, volontairement sans empiler les couches V41/V42/V43 qui avaient été utilisées pour des essais de performance/Agent.

## Contrôles effectués
- 18 blocs JavaScript inline contrôlés avec `node --check` : syntaxe OK.
- Le HTML métier n'est pas transformé par cette version Android.
- Les données Membres/Cotisations/Caisse restent gérées par le noyau web existant.
- Le shell Android conserve JavaScript, DOM Storage, import de fichiers et restauration d'état WebView.
- HTTP non chiffré désactivé (`usesCleartextTraffic=false`).
- Les données privées WebView ne sont pas incluses dans les sauvegardes système Android : l'application conserve son mécanisme de sauvegarde/restauration interne JSON.

## Dépendances réseau encore présentes
Le noyau web référence encore Supabase et des ressources CDN (notamment Supabase JS et Google Fonts). Cette version conserve donc `INTERNET`. Une vraie édition 100 % hors-ligne nécessitera de rapatrier/vendorer ces dépendances avant de supprimer cette permission.

## Compilation
Projet prévu pour Android Gradle Plugin 8.6.1, compileSdk/targetSdk 35 et Java 17.

Ouvrir le dossier dans Android Studio, laisser Gradle synchroniser, puis générer un APK debug ou release.

Cette archive est un projet source Android : elle ne prétend pas être un APK déjà compilé.

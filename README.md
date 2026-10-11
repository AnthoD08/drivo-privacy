# drivo-privacy

Les pages publiques de **Drivo**, hébergées sur Vercel. Fichiers statiques, aucun build.

- `index.html` : support (aide + adresse de contact). C'est la *Support URL* d'App Store Connect.
- `privacy.html` : politique de confidentialité, servie sur `/privacy` (`cleanUrls`). C'est la
  *Privacy Policy URL* d'App Store Connect et le lien `privacy` de `src/lib/links.ts` dans le dépôt Drivo.

Chaque page est en anglais et en français. La langue suit celle de l'appareil ; `#fr` ou `#en`
dans l'URL la force (les fiches App Store FR pointent sur `#fr`).

## Les conditions d'utilisation ne sont pas ici

Drivo pointe sur le **CLUF standard d'Apple**. Tant que l'app n'a ni compte ni service en ligne,
écrire nos propres conditions n'ajouterait rien.

## ⚠️ Ces pages décrivent le comportement réel de l'app

Elles affirment : pas de compte, pas de pub, pas de suivi, pas d'analytics ; seules la position
arrondie (~1 km, vers Apple WeatherKit) et l'état d'abonnement (RevenueCat) quittent l'iPhone.
**Mettre la page à jour AVANT** tout changement qui rendrait ça faux (analytics, pub, ATT,
compte…), et mettre à jour en même temps la section *App Privacy* d'App Store Connect.

Les étapes d'installation du support reprennent les textes de l'app (`setup.*` dans
`src/i18n/locales`) : si l'app change ses libellés, changer aussi cette page.

## Après tout changement

1. Pousser ici : Vercel redéploie tout seul.
2. Vérifier que les deux URLs répondent et que la date en haut de la confidentialité a bougé.
3. Les URLs doivent rester identiques dans `src/lib/links.ts` **et** dans App Store Connect.

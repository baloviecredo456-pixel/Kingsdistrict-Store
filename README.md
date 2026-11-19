# KingsDistrict® — V2 (prototype front-end)

Boutique streetwear en français, destinée au lancement au Togo, en FCFA, avec paiement à la livraison.

## Fichiers
- `index.html` : structure de la boutique et panneaux de commande/administration.
- `style.css` : mise en page responsive noir et blanc.
- `app.js` : catalogue initial, filtres, recherche, fiches produits, panier, demande de commande et administration locale.

## Démarrer
Ouvrir `index.html` dans un navigateur récent. Pour tester le site en local, aucun serveur n'est nécessaire.

## Fonctions de cette V2
- Catalogue initial de 13 références, avec variantes de couleurs et tailles.
- Recherche et filtres par catégorie.
- Fiches produits et panier avec mémorisation locale.
- Formulaire de demande de commande : nom, téléphone/WhatsApp, ville/quartier et adresse.
- Paiement à la livraison uniquement ; prix et disponibilité non renseignés restent « à définir » / « à confirmer ».
- Précommandes avec délai minimum de 45 jours, modifiable par produit.
- Administration de démonstration : ajouter, modifier, masquer, restaurer et supprimer des produits ; ajouter plusieurs photos ; définir prix, statut, tailles, couleurs et délai ; importer/exporter le catalogue JSON.

## Limites importantes
Cette version reste un prototype front-end. Les données du catalogue, du panier et les photos sont enregistrées dans le navigateur utilisé (localStorage). Elles ne sont pas synchronisées entre appareils et ne constituent pas une sauvegarde serveur. Les demandes de commande sont exportées localement en JSON et ne sont pas encore transmises à KingsDistrict.

L'administration n'est pas sécurisée : le bouton ADMIN ne doit pas être considéré comme un accès privé en production. Avant lancement public, connecter une base de données (par exemple Supabase), mettre en place une authentification admin, des règles d'accès (RLS), le stockage distant des images et une fonction serveur pour enregistrer les commandes. Ne jamais exposer une clé secrète/service_role dans le navigateur.

## Publication GitHub
Importer les quatre fichiers dans le dépôt GitHub `Kingsdistrict-Store`. GitHub Pages peut servir une démonstration statique ; la connexion à une base de données et les fonctions serveur nécessiteront une configuration supplémentaire.

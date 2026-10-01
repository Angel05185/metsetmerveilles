# convivavoice.fr — Le Cercle (apporteurs d'affaires) + bouton Connexion

## Contenu

| Fichier | Rôle |
|---|---|
| `le-cercle.html` | **Nouvelle page** servie sur `https://convivavoice.fr/le-cercle` : présentation du programme d'apporteurs d'affaires (identité de la maison, rôle, parcours, espace partenaire, revenu **sans aucun chiffre**, profils, FAQ, formulaire de candidature). |
| `index.html` | Page d'accueil actuelle (version en ligne du 28/09/2026) avec 5 modifications, listées ci-dessous. |

### Modifications de `index.html`
1. Menu : ajout de **« Le Cercle »** (avant « Démo gratuite ») et de **« 🔒 Connexion »** tout à droite, séparé par un filet.
2. CSS : style du lien Connexion et resserrement du menu entre 901 et 1240 px pour que tout tienne sur une ligne.
3. Menu mobile : ordre Le Cercle → Connexion → bouton « Démo gratuite ».
4. Pied de page, colonne « Nous joindre » : liens « Le Cercle — devenir partenaire » et « Espace partenaire — connexion ».
5. Formulaire de démo : remise de `data-netlify="true" netlify-honeypot="bot-field"` (Netlify retire cet attribut de la page servie ; sans lui, un redéploiement de ce fichier risquerait de casser la détection du formulaire `demo-request`).

## Déploiement (Netlify, projet `convivavoice`)
Le site est déployé par envoi de fichiers (pas de dépôt Git relié). Un déploiement remplace **tout** le site : il faut donc repartir du dossier complet du site (77 fichiers + la fonction `emails`), puis :
1. remplacer `index.html` par celui-ci ;
2. ajouter `le-cercle.html` à la racine ;
3. redéployer comme d'habitude.

Après le déploiement, vérifier :
- `https://convivavoice.fr/le-cercle` s'affiche ;
- Netlify → Forms : un nouveau formulaire **`cercle-candidature`** apparaît (activer une notification e-mail dessus) ;
- le formulaire `demo-request` est toujours listé.

## Choix éditoriaux
- **Nom du programme : « Le Cercle »**, plus évocateur qu'« apporteur d'affaires », qui reste le terme juridique utilisé dans la page et le contrat.
- **Aucun chiffre public** (ni prime, ni pourcentage, ni durée) : la page explique la logique (récompensé à chaque signature, revenu récurrent quand le restaurateur s'engage, suivi dans l'espace) ; le barème est remis lors de l'échange avec Angel, dans le dossier partenaire et le contrat. Un restaurateur qui visite le site ne voit donc rien de sensible.
- **Connexion** : lien vers l'espace apporteurs existant `https://conviva-partenaires.netlify.app/` (connexion par code d'accès personnel).
- Événements Google Analytics : `partner_application` (envoi du formulaire) et `partner_login_click` (clic sur Connexion depuis la page Le Cercle).

## Pistes suivantes
- Adresse d'espace plus élégante : ajouter le domaine `espace.convivavoice.fr` au projet Netlify `conviva-partenaires`, puis mettre à jour les liens.
- Ajouter « Connexion » au menu de `/simulateur` (même charte).
- Créer le dossier partenaire (PDF avec le barème) envoyé après candidature.

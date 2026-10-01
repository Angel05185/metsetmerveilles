# Brief Cowork — Le Cercle + bouton Connexion sur convivavoice.fr (01/10/2026)

## Contexte
Ajout sur convivavoice.fr d'un programme d'apporteurs d'affaires appelé **« Le Cercle »** et d'un accès **« Connexion »** à l'espace apporteurs existant. Les fichiers sont prêts et ont été testés sur ordinateur, tablette et mobile. **Ils ne sont pas encore en ligne.**

## Fichiers (dépôt GitHub public, branche `claude/tender-lovelace-txph41`, dossier `convivavoice/`)
- `le-cercle.html` → https://raw.githubusercontent.com/Angel05185/metsetmerveilles/claude/tender-lovelace-txph41/convivavoice/le-cercle.html
- `index.html` → https://raw.githubusercontent.com/Angel05185/metsetmerveilles/claude/tender-lovelace-txph41/convivavoice/index.html
- `README.md` (détail technique) → https://raw.githubusercontent.com/Angel05185/metsetmerveilles/claude/tender-lovelace-txph41/convivavoice/README.md

## Ce qui a été fait
1. **Nouvelle page `/le-cercle`** (fichier `le-cercle.html`), dans la charte du site (terracotta/crème, Fraunces + Inter) :
   - la maison Conviva : « L'art de ne jamais manquer une table », avec 3 valeurs (respect du métier, honnêteté, relation qui dure) ;
   - le rôle : le partenaire repère, rencontre, fait écouter la démo et transmet ; Conviva signe, installe en 48 h, facture et accompagne ; il ne signe rien, n'encaisse rien et ne négocie rien ;
   - le parcours : échange avec Angel, puis contrat et accès à l'espace, puis 4 semaines de formation, puis le terrain avec un point régulier ;
   - l'espace partenaire : aperçu illustratif du logiciel (noms fictifs) ;
   - le revenu, **sans aucun chiffre** : « reconnu à chaque signature », « un revenu qui dure », « clair et suivi ». Le barème est remis uniquement lors de l'échange, dans le dossier partenaire et dans le contrat ;
   - les profils recherchés (6), une FAQ (6 questions) et un formulaire Netlify **`cercle-candidature`** (bouton « Recevoir le dossier partenaire ») ;
   - le suivi Google Analytics : `partner_application` et `partner_login_click`.
2. **Accueil (`index.html`, à partir de la version en ligne du 28/09/2026)** :
   - menu en haut à droite : « Le Cercle » avant « Démo gratuite », et « 🔒 Connexion » tout à droite, qui ouvre https://conviva-partenaires.netlify.app/ ;
   - menu mobile dans l'ordre : Le Cercle, Connexion, puis le bouton Démo ;
   - pied de page : liens « Le Cercle — devenir partenaire » et « Espace partenaire — connexion » ;
   - formulaire de démo : remise de l'attribut `data-netlify="true"`, retiré par Netlify dans la page servie. Indispensable pour ne pas casser le formulaire `demo-request`.

## Décisions validées
- Nom du programme : **Le Cercle**. Le terme juridique « apporteur d'affaires » reste dans la page et dans le contrat.
- Aucun chiffre de rémunération en public : les clients restaurateurs ne doivent rien voir de sensible.
- La connexion se fait sur l'espace existant `conviva-partenaires` (code d'accès personnel).

## À faire pour la mise en ligne (projet Netlify `convivavoice`)
Le site est déployé par envoi de fichiers : un déploiement remplace **tout** le site. Il faut donc partir du dossier complet actuel (77 fichiers + la fonction `emails`), puis :
1. remplacer `index.html` par le nouveau ;
2. ajouter `le-cercle.html` à la racine ;
3. redéployer ;
4. vérifier que https://convivavoice.fr/le-cercle s'affiche ;
5. vérifier dans Netlify → Forms que `cercle-candidature` apparaît et que `demo-request` est toujours là, puis activer une notification e-mail sur `cercle-candidature`.

## Prochaines étapes proposées
- Créer le **dossier partenaire en PDF** (avec le barème), à envoyer après chaque candidature.
- Brancher le domaine **espace.convivavoice.fr** sur le projet Netlify `conviva-partenaires`, puis mettre à jour les liens « Connexion ».
- Ajouter « Connexion » au menu de la page `/simulateur`.
- Mettre à jour les documents du projet Conviva (présentation du site, plan commercial, recrutement des apporteurs) avec : le nom « Le Cercle », l'URL `/le-cercle` et le formulaire `cercle-candidature`.

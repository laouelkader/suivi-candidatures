# Suivi de candidatures

Un site d'une seule page : tu charges ton fichier Excel et il construit tout seul ton tableau de bord (statuts, relances à faire, rythme d'envoi, recherche et filtres). Il n'y a pas de serveur : le fichier est lu dans ton navigateur et rien n'est envoyé sur Internet.

## Mettre le site en ligne avec GitHub Pages

1. Sur github.com, crée un dépôt (bouton « New »), par exemple `suivi-candidatures`.
2. Clique sur « uploading an existing file » et dépose ces fichiers à la racine du dépôt :
   - `index.html`
   - `xlsx.full.min.js`
   - `xlsx.LICENSE.txt`
   - `README.md`
3. Valide avec « Commit changes ».
4. Va dans **Settings → Pages**. Sous « Build and deployment », choisis **Deploy from a branch**, branche **main**, dossier **/ (root)**, puis **Save**.
5. Après une à deux minutes, le site est disponible à l'adresse `https://TON-PSEUDO.github.io/suivi-candidatures/`.

## Utilisation

- Ouvre le site, clique sur « Choisir un fichier » (ou glisse ton Excel dans la page).
- Pour mettre à jour : modifie ton Excel, puis recharge-le sur le site.
- Le site garde les dernières données dans le navigateur (sur cet appareil seulement). Le bouton « Effacer les données » les supprime.
- « Télécharger un modèle » donne un fichier Excel vide avec les bonnes colonnes.

## Format du fichier Excel

Une ligne par candidature, avec les en-têtes sur la première ligne. Colonnes reconnues (seule « Entreprise » ou « Poste » est obligatoire) :

| Colonne | Contenu |
|---|---|
| Entreprise | Nom de l'employeur |
| Poste | Intitulé de l'offre |
| Type | Alternance, Stage… |
| Lieu | Ville |
| Date de candidature | JJ/MM/AAAA |
| Canal | Indeed, site de l'entreprise, e-mail… |
| Statut | En attente, Entretien, Offre, Refus, Non finalisée, Non confirmée |
| Dernier retour | Date du dernier mail reçu |
| Relance conseillée le | Date de relance (sinon : date de candidature + 10 jours) |
| Notes | Texte libre |

Si ton classeur a plusieurs onglets, le site lit celui dont le nom contient « Candidatures ». Ton fichier `Suivi_candidatures_Laouel.xlsx` est déjà au bon format.

## Confidentialité

- Le dépôt GitHub Pages est public par défaut : n'y mets **pas** ton fichier Excel. Seuls les fichiers du site doivent y figurer.
- La page demande aux moteurs de recherche de ne pas l'indexer, mais toute personne qui connaît l'adresse peut l'ouvrir. Elle n'y verra que la page vide, puisque tes données restent sur ton appareil.

## Licence

La lecture des fichiers Excel utilise la bibliothèque SheetJS (version 0.18.5, licence Apache 2.0), incluse dans `xlsx.full.min.js`.

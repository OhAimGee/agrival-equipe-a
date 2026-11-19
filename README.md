# Mission AGRIVAL · tableau de bord de l'équipe A

Page unique (`index.html`) qui suit l'avancement de l'équipe A, phase par phase (SAP Activate), avec une vue « Aujourd'hui » pour les trois membres. Les cases cochées sont enregistrées dans le dépôt GitHub (fichier `data/progress.json` sur la branche `progress-data`), donc chacun voit l'avancement des autres.

Dashboard d'avancement du projet de fin de formation de consultant SAP.

**Page en ligne :** https://ohaimgee.github.io/agrival-equipe-a/

## Jeton d'écriture de l'équipe (une seule fois, par Raph)

Sur GitHub, *Settings* du compte (pas du dépôt) > *Developer settings* > *Personal access tokens* > *Fine-grained tokens* > *Generate new token* :
- *Expiration* : 30 jours (le jeu se termine le 02/12) ;
- *Repository access* : *Only select repositories*, choisir **uniquement** `agrival-equipe-a` ;
- *Permissions > Repository permissions > Contents* : **Read and write** (rien d'autre).

Copier le jeton (`github_pat_…`) et l'envoyer à Nounedia et Nadia en message privé, jamais dans un canal public ni dans le dépôt.

## Utilisation (chaque membre, une fois par navigateur)

1. Ouvrir l'adresse GitHub Pages.
2. Bouton **Paramètres** : choisir son nom dans « Je suis », coller le jeton, **Enregistrer et tester**. Le propriétaire et le nom du dépôt sont détectés seuls depuis l'adresse.
3. Cocher ses tâches et sa routine du jour. L'indicateur en haut affiche « Synchronisé » ; la page relit l'avancement des autres chaque minute et à chaque retour sur l'onglet.

Sans jeton, la page fonctionne en **lecture seule** : utile pour la montrer à quelqu'un d'autre.

## Bon à savoir

- Le jeton reste dans le navigateur de chacun (stockage local) ; il n'est jamais écrit dans le dépôt. « Oublier le jeton » l'efface. En cas de fuite, le supprimer dans GitHub et en créer un nouveau.
- Toutes les écritures apparaissent dans l'historique sous le compte de Raph ; la page enregistre qui a coché quoi (nom et heure affichés sous chaque tâche).
- Deux personnes qui cochent au même moment ne s'écrasent pas : la page relit le fichier et refait l'écriture.
- Les cases sont enregistrées sur la branche `progress-data`, séparée de `main`, pour ne pas relancer la publication de la page à chaque clic.
- Ouverte en local (double-clic sur le fichier), la page fonctionne en mode local : les cases ne sont visibles que sur cet appareil.
- Ne jamais écrire de mot de passe SAP sur la page ni dans le dépôt (il est public).
- Pour modifier les tâches : éditer le tableau `tasks` dans `index.html` (chaque tâche a un `id` stable ; changer un `id` fait perdre sa case cochée).

# Mode d’emploi du portfolio

Ce fichier ne s’affiche pas sur le site. Il explique comment tout faire depuis le navigateur, sans coder.

## 1. Mettre le site en ligne (une seule fois)

1. Sur GitHub, ouvre le dépôt `morgane-le-touze.github.io`.
2. Clique sur **Add file → Upload files**.
3. Décompresse `portfolio-site.zip`, ouvre le dossier obtenu, sélectionne **tout son contenu** (pas le dossier lui-même) et glisse-le dans la page. Les dossiers qui commencent par `_` doivent bien partir aussi.
4. En bas, clique sur **Commit changes**.
5. Va dans **Settings → Pages**. Sous *Build and deployment*, choisis **Deploy from a branch**, branche **main**, dossier **/ (root)**, puis **Save**.
6. Attends une ou deux minutes : le site est sur https://morgane-le-touze.github.io

L’onglet **Actions** du dépôt montre la mise à jour en cours : rond orange = en cours, coche verte = en ligne, croix rouge = erreur (voir la section 7).

## 2. Corriger une virgule

1. Ouvre le fichier, par exemple `_articles/meizu-21-note.md`.
2. Clique sur le crayon ✏️ en haut à droite du fichier.
3. Corrige, puis **Commit changes**. Le site se met à jour seul en une à deux minutes.

## 3. Ajouter un article

1. **Les photos** : sur ton ordinateur, crée un dossier au nom de l’article, sans espaces ni accents (ex. `galaxy-z-fold8-ultra`). Mets-y les photos, plus une **vignette** pour la grille, nommée `vignette.jpg`, de préférence à l’horizontale (format 3:2). Sinon elle sera recadrée au centre.
   Conseil : réduis les photos à 1600 pixels de large au maximum avant de les envoyer, sinon les pages seront lentes.
2. Dans le dépôt, ouvre `assets/images`, puis **Add file → Upload files** et glisse le dossier entier.
3. Ouvre le dossier `_articles`, puis **Add file → Create new file**. Nomme-le comme le dossier photos, avec `.md` à la fin (ex. `galaxy-z-fold8-ultra.md`). Ce nom devient l’adresse de la page.
4. Copie-colle le contenu de `MODELE-ARTICLE.md` (à la racine du dépôt) et remplace les textes.
5. **Commit changes**.

## 4. Changer l’ordre des articles

Chaque article a une ligne `ordre:` dans son bloc du haut. Le plus petit nombre apparaît en premier dans la grille. Pour mettre un article en tête, donne-lui `ordre: 0`, ou renumérote les autres.

## 5. Masquer ou supprimer un article

- **Masquer sans supprimer** : ajoute la ligne `published: false` dans le bloc du haut. Pour le remettre, supprime la ligne.
- **Supprimer** : ouvre le fichier dans `_articles`, menu **…** en haut à droite → **Delete file**. Pense à supprimer aussi son dossier de photos dans `assets/images`.

## 6. Changer l’accroche, le mail ou LinkedIn

Tout est dans `_config.yml`, en haut, entre guillemets : `accroche`, `sous_accroche`, `email`, `linkedin`.

La ligne `indexer: false` demande aux moteurs de recherche de ne pas référencer le site. Passe-la à `indexer: true` quand tu veux apparaître dans Google. La page À propos est dans `a-propos.md`.

## 7. Comment écrire un article

| Je veux… | J’écris… |
|---|---|
| un intertitre | `## Titre` (sous-titre : `### Titre`) |
| du gras | `**texte**` |
| de l’italique | `*texte*` |
| un lien | `[texte cliquable](https://adresse)` |
| une photo | `![description de la photo](/assets/images/dossier/photo.jpg)` |
| une légende | la ligne juste sous la photo, en `*italique*`, sans ligne vide entre les deux |
| deux images côte à côte | deux lignes d’image l’une sous l’autre, sans ligne vide |
| une note grise (sources) | un paragraphe entier en `*italique*` |
| l’encadré rose | voir « Conditions du test » dans le modèle, avec `{: .encadre}` en dessous |
| le bloc prune du verdict | voir la fin du modèle, avec `{: .verdict}` en dessous |

Un nouveau paragraphe = une ligne vide.

**Le bloc du haut (entre les deux `---`) est le plus fragile.** Garde les guillemets droits `"` autour du titre et du chapô. Si ton texte contient lui-même un guillemet droit `"`, remplace-le par « » ou par “ ”.

**En cas de croix rouge dans Actions** : clique dessus, l’erreur indique souvent le fichier et la ligne. Neuf fois sur dix, c’est un guillemet ou un deux-points dans le bloc du haut.

## 8. À savoir

- **La police** n’est pas Freight Neo Pro : celle-ci dépend d’un abonnement Adobe et ne peut pas être hébergée sur le site. C’est **Alegreya Sans**, gratuite (licence SIL OFL), stockée dans `assets/fonts`. Elle ne dépend d’aucun service extérieur.
- **Les couleurs** sont en haut de `assets/css/style.css`.
- **Le dépôt est public** : tout ce que tu y déposes est visible par tout le monde, y compris ce fichier.

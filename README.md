# AccèsTech – site vitrine

Site statique (HTML/CSS, sans dépendance ni cookie) pour GitHub Pages.

## Contenu

- `index.html` : page d'accueil (services, tarifs, déroulement, zone, contact)
- `mentions-legales.html` : mentions légales
- `style.css`, `logo.png`, `favicon.png`, `CNAME`

## À compléter avant mise en ligne

Chercher `À COMPLÉTER` / `exemple.fr` / `00 00 00 00 00` dans `index.html` et `mentions-legales.html` :
e-mail, téléphone, identité civile, SIRET (après le 01/01/2027), TVA, médiateur de la consommation.

## Déploiement sur GitHub Pages

1. Créer un dépôt GitHub (ex. `accestech`), y déposer ces fichiers à la racine.
2. Settings → Pages → Source : « Deploy from a branch », branche `main`, dossier `/ (root)`.
3. Le fichier `CNAME` (contenant `acces-tech.com`) est déjà à la racine.
   Settings → Pages → Custom domain : vérifier que `acces-tech.com` est bien saisi, puis Save.
4. Chez le registrar de `acces-tech.com`, ajouter les enregistrements DNS :
   - Domaine nu (apex, `@`) : 4 enregistrements `A` vers `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - Sous-domaine `www` : `CNAME` vers `<ton-compte>.github.io`
     (GitHub redirige alors `www.acces-tech.com` vers `acces-tech.com`)
   - Vérifier la liste d'IP à jour dans la doc GitHub Pages.
5. Attendre la propagation DNS (de quelques minutes à 24 h), puis cocher « Enforce HTTPS ».

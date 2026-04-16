# Guide de mise en ligne — vie.epbse.org

## Contenu du dossier
- index.html — app complète (Vie EPBSE)
- manifest.json — config PWA
- sw.js — mode hors-ligne
- CNAME — indique à GitHub le domaine vie.epbse.org
- icons/ — icônes Android
- .github/workflows/deploy.yml — déploiement automatique

---

## 1. Créer le dépôt GitHub
1. Connecte-toi sur github.com avec le compte epbstetienne-42
2. Cliquer + (haut droite) → New repository
3. Nom : vie-epbse
4. Visibilité : Public (obligatoire)
5. Ne cocher rien → Create repository

## 2. Uploader les fichiers
Sur la page du dépôt vide, cliquer "uploading an existing file"
Glisser-déposer : index.html, manifest.json, sw.js, CNAME, dossier icons/

Pour .github/workflows/deploy.yml :
- Cliquer Create new file
- Taper dans le nom : .github/workflows/deploy.yml
- Coller le contenu du fichier deploy.yml
- Commit new file

## 3. Activer GitHub Pages
Settings → Pages → Source : GitHub Actions
URL temporaire : https://epbstetienne-42.github.io/vie-epbse

## 4. DNS chez ton registrar
Ajouter un enregistrement CNAME :
- Nom/Hôte : vie
- Valeur : epbstetienne-42.github.io.
- TTL : 3600

## 5. Lier le domaine dans GitHub
Settings → Pages → Custom domain → vie.epbse.org → Save
Cocher Enforce HTTPS
Propagation DNS : 5 à 30 minutes

## 6. Installer sur Android
Chrome → vie.epbse.org → "Ajouter à l'écran d'accueil"

## Personnalisation
- Code PIN admin : chercher PIN_CODE = '1905' et remplacer par ton code
- Remplacer les noms fictifs par les vrais bénévoles
- Modifier les événements pré-remplis

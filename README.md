# Site Isabelle FAR. — Facialiste · Kobido

Site vitrine de **Isabelle FAR.**, facialiste certifiée Kobido à Cesson-Sévigné (35).

---

## 1. Ce qu'est ce projet (et ce qu'il n'est pas)

C'est un **site statique**. Concrètement :

- Aucune installation, aucun `npm install`, aucun logiciel à acheter.
- Aucun serveur applicatif, aucune base de données, aucun compte à créer.
- Aucune variable d'environnement, aucune clé d'API, aucun mot de passe.
- Tout le site tient dans **un seul fichier** `index.html` (HTML + CSS + JavaScript
  réunis), accompagné de deux dossiers de médias.

Conséquence pratique : pour mettre le site en ligne, il suffit de **déposer les
fichiers chez un hébergeur**. Rien d'autre.

---

## 2. Contenu du dossier

```
index.html          ← le site entier (textes, styles, animations)
images/             ← 15 photos et illustrations
videos/             ← les 2 fichiers du logo animé
README.md           ← ce document
```

### Fichiers indispensables

Le site **ne fonctionne pas** si l'un de ces fichiers manque :

| Dossier | Fichiers |
|---|---|
| racine | `index.html` |
| `images/` | `fond-seamless.jpg`, `logo.png`, `portrait.jpg`, `maison.jpg`, `cabinet.jpg`, `huile.jpg`, `anatomie.jpg`, `diplome.jpg`, `histoire.jpg`, `kobido.jpg`, `kogao.jpg`, `drainage.jpg`, `atama.jpg`, `forfait-essentiel.jpg`, `forfait-excellence.jpg` |
| `videos/` | `logo-anim.webp`, `logo-anim-mobile.webp` |

> ⚠️ **Le dossier `videos/` est obligatoire.** Il contient le logo animé de la
> page d'accueil. Si vous ne mettez en ligne que `index.html` et `images/`,
> le logo du haut de page ne s'affichera pas.

---

## 3. Voir le site sur votre ordinateur

Double-cliquez sur `index.html`. Il s'ouvre dans votre navigateur. C'est tout.

---

## 4. Mettre le site en ligne

### Option A — Hébergement gratuit, en 2 minutes

1. Allez sur <https://app.netlify.com/drop>
2. Glissez-y le **dossier complet** (avec `images/` **et** `videos/`)
3. Vous obtenez immédiatement une adresse publique

### Option B — Avec le nom de domaine `isabelle-far.fr`

1. Achetez le domaine chez un registrar (OVH, Gandi, Infomaniak…)
2. Déposez le dossier chez votre hébergeur, ou reliez le domaine à Netlify
   (*Domain settings → Add custom domain*)
3. Vérifiez que le certificat **HTTPS** est bien activé (gratuit et automatique
   chez la plupart des hébergeurs)

### Option C — Hébergement classique (FTP)

Envoyez le contenu du dossier dans le répertoire public de votre hébergement
(souvent nommé `www/`, `public_html/` ou `htdocs/`), en **conservant la
structure des dossiers**.

---

## 5. Modifier le site

Ouvrez `index.html` avec un éditeur de texte. Le Bloc-notes fonctionne, mais
[VS Code](https://code.visualstudio.com) (gratuit) est bien plus confortable :
il colore le code et permet de chercher facilement.

> 💾 **Faites toujours une copie de sauvegarde de `index.html` avant de modifier.**

### Changer un texte

`Ctrl+F` pour chercher le texte actuel → remplacez-le → `Ctrl+S` pour enregistrer.

### Changer une photo

Placez votre nouvelle image dans `images/` en lui donnant **exactement le même
nom** que l'ancienne. Le site la prendra automatiquement.

| Fichier | Emplacement sur le site |
|---|---|
| `portrait.jpg` | photo de la rubrique « Qui suis-je » |
| `diplome.jpg` | remise de diplôme |
| `maison.jpg`, `cabinet.jpg`, `huile.jpg`, `anatomie.jpg` | rubrique « Informations pratiques » |
| `kobido.jpg`, `kogao.jpg`, `drainage.jpg`, `atama.jpg` | une par prestation |
| `forfait-essentiel.jpg`, `forfait-excellence.jpg` | les forfaits |
| `histoire.jpg` | rubrique « Le saviez-vous ? » |
| `logo.png` | logo de la barre de navigation |
| `fond-seamless.jpg` | image de fond (bambous) |

### Ajouter ou supprimer une prestation

Cherchez `<div class="scard fade-up">` : c'est le début d'une carte de soin.

- **Supprimer** : effacez tout le bloc, depuis `<div class="scard fade-up">`
  jusqu'à son `</div>` de fermeture.
- **Ajouter** : copiez un bloc existant, collez-le, puis changez le nom, la
  durée, le prix et la description.

Même principe pour les forfaits : cherchez `<div class="forfait fade-up">`.

### Modifier les tarifs

- Sur les cartes de soin : cherchez `scard-price`
- Dans le tableau récapitulatif : cherchez `<table class="price-table"`

### Mentions légales et coordonnées

Tout est en bas de page. Cherchez `SIRET`, `Code APE`, `TVA`,
`isabelle.far35@gmail.com` ou `06 20 43 78 41`.

---

## 6. À compléter avant la mise en ligne publique

Ces trois mentions sont **obligatoires en France** et sont actuellement
renseignées « en attente » dans le pied de page :

- [ ] Numéro **SIRET**
- [ ] **Code APE**
- [ ] **Numéro de TVA intracommunautaire**

Autres points à prévoir :

- [ ] **Politique de confidentialité** — obligatoire dès lors que le site
      collecte des données ou dépose des cookies. Le site n'en dépose aucun
      aujourd'hui (voir §7), mais tout ajout ultérieur (formulaire de contact,
      Google Analytics, pixel Meta) la rendra nécessaire, ainsi qu'un bandeau
      de consentement.
- [ ] Vérifier que les **liens de réservation** pointent vers la bonne fiche
      Glaads, et que les prestations y sont bien publiées.

---

## 7. Données personnelles et sécurité

État actuel du site :

- **Aucun formulaire**, aucun champ de saisie → aucune donnée visiteur collectée.
- **Aucun cookie**, aucun traceur, aucune statistique.
- **Aucun compte utilisateur**, aucune authentification.
- **Aucune clé d'API ni secret** dans le code.

Le site charge en revanche les polices **Google Fonts depuis les serveurs de
Google**, ce qui transmet l'adresse IP des visiteurs à Google. Cette pratique a
été jugée non conforme au RGPD par plusieurs autorités européennes. La solution
consiste à **héberger les polices avec le site** — voir avec votre développeur.

---

## 8. Référencement (SEO)

Déjà en place : titre de page, méta-description, URL canonique, balises de
partage social (Open Graph), attributs `alt` sur toutes les images, structure de
titres cohérente (un seul `<h1>`, neuf `<h2>`).

Manquent encore, à faire avant ou juste après la mise en ligne :

- Attribut `lang="fr"` sur la page (indique la langue aux moteurs de recherche)
- Une **favicon** (icône affichée dans l'onglet du navigateur)
- Des **données structurées** `LocalBusiness` — très utile pour un commerce
  local : elles permettent à Google d'afficher l'adresse, les horaires et les
  avis directement dans les résultats
- Un fichier `robots.txt` et un `sitemap.xml`
- Créer et vérifier la fiche **Google Business Profile**, puis la relier au site

---

## 9. Licence

Ce site appartient à Isabelle FAR. Vous êtes libre de le modifier, de l'héberger
et de le diffuser sans restriction.

Conception & réalisation : **Agence M2** — Malo & Miguel

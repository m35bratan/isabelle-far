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
modifier.html       ← votre espace de modification (voir §5)
images/             ← photos et illustrations
fonts/              ← les polices d'écriture du site
README.md           ← ce document
```

### Fichiers indispensables

Le site **ne fonctionne pas** si l'un de ces fichiers manque :

| Dossier | Fichiers |
|---|---|
| racine | `index.html` |
| `images/` | `fond-seamless.webp`, `logo.png`, `logo-hero.png`, `portrait.jpg`, `maison.jpg`, `cabinet.jpg`, `huile.jpg`, `diplome.jpg`, `histoire.jpg`, `kobido.jpg`, `kogao.jpg`, `drainage.jpg`, `atama.jpg` |

> ℹ️ **Le dossier `videos/` n'est plus utilisé.** Le logo de la page d'accueil
> était auparavant une image animée ; c'est désormais une image fixe,
> `images/logo-hero.webp`. Vous pouvez supprimer le dossier `videos/`.

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

### Option D — GitHub Pages *(recommandé si vous voulez modifier le site vous-même)*

C'est la seule option où **modifier le site et le publier sont le même geste** :
vous corrigez un texte depuis votre navigateur, et la mise en ligne se fait
toute seule une minute plus tard. Voir §5 pour la marche à suivre.

Adresse obtenue : `https://COMPTE.github.io/isabelle-far/`

---

## 5. Modifier le site

Trois façons de faire. **La première est de loin la plus simple.**

### ⭐ Méthode A — L'espace de modification *(aucune connaissance technique)*

**👉 <https://m35bratan.github.io/isabelle-far/modifier.html>**

Une page privée, avec des formulaires : vous tapez votre texte dans des cases,
vous cliquez sur **Publier**, et le site se met à jour tout seul. Aucun code
n'est visible. Fonctionne aussi bien sur ordinateur que sur téléphone.

**Ce que vous pouvez changer :**

| Rubrique | Contenu modifiable |
|---|---|
| Accueil | la phrase d'accroche |
| Mes soins | nom, durée, prix et description des 4 soins |
| Tarifs | les 5 lignes du tableau |
| Forfaits | nom, contenu, prix des 2 forfaits |
| Horaires | les 4 lignes d'horaires |
| Recommandations | les consignes avant le rendez-vous |
| Qui suis-je | votre présentation |
| Le saviez-vous | la légende du Kobido |
| Avis clientes | les 4 témoignages |
| Réseaux | pseudo Instagram et Facebook |
| Mentions légales | SIRET, code APE, TVA, capital |
| Photos | les 12 photos du site |

**Première connexion — à faire une seule fois.** La page vous demande une
« clé d'accès » qui l'autorise à modifier votre site. Pour la créer :

1. Ouvrez <https://github.com/settings/personal-access-tokens/new>
2. *Token name* : `Site Isabelle`
3. *Expiration* : `No expiration`
4. *Repository access* : `Only select repositories` → choisissez `isabelle-far`
5. *Permissions → Repository permissions → Contents* : `Read and write`
6. Cliquez sur **Generate token**, copiez la clé affichée
7. Collez-la dans l'espace de modification

La clé reste **enregistrée sur votre appareil uniquement** : vous ne la
retaperez plus. Ne la communiquez à personne. En cas de doute, supprimez-la
depuis GitHub et recréez-en une.

> 💡 Les photos que vous envoyez sont **automatiquement redimensionnées** :
> vous pouvez utiliser directement une photo prise avec votre téléphone.

> ⏱️ Après avoir cliqué sur *Publier*, comptez **une minute** avant de voir
> le changement en ligne. Rechargez la page du site si besoin.

### 🟢 Méthode B — Depuis GitHub, dans votre navigateur *(rien à installer)*

Pour les changements que l'espace de modification ne couvre pas (ajouter un
soin entier, changer un lien, modifier la mise en page) :

C'est la méthode à privilégier : aucun logiciel, aucune manipulation de
fichiers, **aucun risque de casser la version en ligne**, et chaque
modification est publiée automatiquement.

**Changer un texte, un tarif, un horaire :**

1. Ouvrez le dépôt sur GitHub et cliquez sur `index.html`
2. Cliquez sur l'icône **crayon** ✏️ en haut à droite
3. `Ctrl+F` pour trouver le texte à changer, modifiez-le
4. Descendez en bas, bouton vert **Commit changes**
5. Attendez environ une minute : le site en ligne est à jour

**Remplacer une photo :**

1. Ouvrez le dossier `images/` sur GitHub
2. Bouton **Add file → Upload files**
3. Déposez votre nouvelle image, en lui donnant **exactement le même nom**
   que celle à remplacer (voir le tableau plus bas)
4. **Commit changes**

**Revenir en arrière si vous vous êtes trompée :**

Onglet **Commits** → choisissez une version précédente → bouton **Revert**.
Rien n'est jamais perdu : chaque modification est enregistrée et réversible.
C'est le principal avantage de cette méthode.

> 💡 Astuce : dans le dépôt, appuyez sur la touche **`.`** (point) de votre
> clavier. Un véritable éditeur de code s'ouvre dans le navigateur, plus
> confortable pour les modifications un peu longues.

### 🔵 Méthode C — Sur votre ordinateur

Ouvrez `index.html` avec un éditeur de texte. Le Bloc-notes fonctionne, mais
[VS Code](https://code.visualstudio.com) (gratuit) est bien plus confortable :
il colore le code et permet de chercher facilement.

> 💾 **Faites toujours une copie de sauvegarde de `index.html` avant de modifier.**

> ⚠️ Avec cette méthode, vos modifications restent **sur votre ordinateur**.
> Le site en ligne ne changera pas tant que vous n'aurez pas renvoyé les
> fichiers à votre hébergeur. Si vous utilisez GitHub, préférez la méthode A :
> les deux versions resteront identiques.

### Changer un texte

`Ctrl+F` pour chercher le texte actuel → remplacez-le → `Ctrl+S` pour enregistrer.

### Changer une photo

Placez votre nouvelle image dans `images/` en lui donnant **exactement le même
nom** que l'ancienne. Le site la prendra automatiquement.

| Fichier | Emplacement sur le site |
|---|---|
| `portrait.jpg` | photo de la rubrique « Qui suis-je » |
| `diplome.jpg` | remise de diplôme |
| `maison.jpg`, `cabinet.jpg`, `huile.jpg` | rubrique « Informations pratiques » |
| `kobido.jpg` | prestation « Authentique KOBIDO Lift » |
| `kogao.jpg` | prestation « KOGAO » **et** forfait « Essentiel » |
| `drainage.jpg` | prestation « KOGAO/Drainage visage » |
| `atama.jpg` | prestation « KOBIDO Sculpting » **et** forfait « Excellence » |
| `histoire.jpg` | rubrique « Le saviez-vous ? » |
| `logo.png` | logo de la barre de navigation |
| `logo-hero.png` | grand logo de la page d'accueil (PNG détouré, fond transparent) |
| `fond-seamless.webp` | image de fond (bambous) |

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

Ces trois mentions **obligatoires en France** sont désormais renseignées dans
le pied de page :

- [x] Numéro **SIRET** — 107 510 430 00013
- [x] **Code APE** — 9604Z
- [x] **Numéro de TVA intracommunautaire** — TVA non applicable

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

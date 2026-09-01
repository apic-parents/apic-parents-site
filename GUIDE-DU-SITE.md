# Guide du site internet de l'APIC

**À lire par toute personne qui reprend la gestion du site.**
Ce guide explique où se trouve le site, comment il fonctionne, et comment le modifier — sans connaissances techniques particulières.

Adresse du site : **https://apic-parents.github.io/apic-parents-site/**

---

## 1. En deux mots : comment ça marche

Le site n'est pas hébergé chez un prestataire payant. Il est hébergé **gratuitement par GitHub**, grâce à un service appelé *GitHub Pages*.

Le principe est simple :

1. Tous les fichiers du site (textes, photos, mise en page) sont rangés dans un « dépôt » — un dossier en ligne — appelé **`apic-parents-site`**.
2. Dès qu'un fichier est modifié dans ce dépôt, GitHub **reconstruit automatiquement le site** et le met en ligne.
3. La mise à jour est visible sur le site public au bout d'**une à deux minutes**.

Il n'y a donc rien à « publier », rien à envoyer par FTP, aucun logiciel à installer. **Modifier un fichier sur GitHub = mettre le site à jour.**

Le site est construit avec **Jekyll**, un outil intégré à GitHub Pages qui transforme des fichiers texte en pages web. C'est ce qui permet, par exemple, qu'un nouvel article apparaisse tout seul sur la page d'accueil *et* sur la page de son établissement, sans avoir à toucher à ces pages.

> **Coût : 0 €.** GitHub Pages est gratuit pour ce type de site. Il n'y a pas d'abonnement à renouveler, pas de facture, pas de date d'expiration. Le seul risque de disparition serait la perte d'accès au compte GitHub — d'où l'importance de la section 8.

---

## 2. Les trois outils à connaître

| Outil | À quoi il sert | Adresse |
|---|---|---|
| **GitHub** | Héberge le site et tous ses fichiers. C'est là qu'on modifie les pages, les photos, les textes. | https://github.com/apic-parents/apic-parents-site |
| **Pages CMS** | Interface simplifiée pour **écrire les actualités** sans voir de code. C'est l'outil du quotidien. | https://pagescms.org/ |
| **HelloAsso** | Gère les adhésions en ligne (12 € par famille). Le site pointe vers HelloAsso par des liens. | https://www.helloasso.com/associations/apic31 |

Les identifiants de connexion **ne figurent pas dans ce guide** (il est public). Voir la section 8.

---

## 3. Écrire une actualité — la tâche la plus courante

**C'est la seule chose à savoir pour faire vivre le site au quotidien.** Aucune compétence technique n'est nécessaire.

### La marche à suivre

1. Aller sur **https://pagescms.org/**
2. Cliquer sur **« Sign in with GitHub »** et se connecter avec le compte GitHub de l'APIC.
3. Choisir le dépôt **`apic-parents-site`**.
4. Dans le menu de gauche, cliquer sur **« Actualités »**. La liste des articles existants s'affiche.
5. Cliquer sur **« Add an entry »** (ajouter un article) — ou sur un article existant pour le corriger.
6. Remplir les champs (détaillés ci-dessous).
7. Cliquer sur **« Save »**. C'est tout : l'article est en ligne une à deux minutes plus tard.

### Les champs à remplir

| Champ | Obligatoire | Explication |
|---|---|---|
| **Titre** | oui | Le titre de l'article, tel qu'il apparaîtra. |
| **Date** | oui | La date de l'article. Elle détermine l'ordre d'affichage : le plus récent en premier. |
| **Identifiant pour l'adresse** | oui | Sert à construire l'adresse web de l'article. **En minuscules, avec des tirets, sans accent ni espace.** Exemple : `vente-de-gateaux-mars`. |
| **Établissement concerné** | oui | À choisir dans la liste. Voir l'encadré ci-dessous, c'est important. |
| **Thème** | non | Un mot-clé affiché à côté de la date : `Travaux`, `Cantine`, `Vente`, `Adhésions`… Libre. |
| **Image principale** | non | Une photo d'illustration en haut de l'article. |
| **Résumé** | non mais **fortement conseillé** | Deux ou trois lignes. **C'est ce texte qui s'affiche sur la page d'accueil** pour donner envie de lire. Sans résumé, la vignette de l'article paraît vide. |
| **Fichiers joints** | non | Pour proposer un PDF en téléchargement (compte rendu, bulletin…). On peut en mettre plusieurs, chacun avec un nom affiché. |
| **Contenu de l'article** | oui | Le texte. L'éditeur permet de mettre en gras, en italique, de faire des listes, des titres et des liens. |

> ### ⚠️ Le champ « Établissement concerné » : à bien comprendre
>
> Ce champ ne sert pas seulement à afficher une étiquette. **Il décide sur quelles pages l'article apparaît :**
>
> - Un article marqué **« Collège Michelet »** apparaît sur la page d'accueil **et** sur la page du collège Michelet — et sur elle seule.
> - Un article marqué **« Toutes sections »** apparaît sur la page d'accueil **et sur les six pages d'établissement**.
>
> Choisissez donc « Toutes sections » uniquement pour ce qui concerne vraiment toutes les familles (adhésions, assemblée générale, vœux…), sinon les pages d'établissement se remplissent d'informations qui ne les concernent pas.

### Pour supprimer un article

Dans Pages CMS, ouvrir l'article, puis le menu **« … »** en haut à droite et **« Delete »**.

---

## 4. Modifier le reste du site

Tout le reste (textes des pages, photos, contacts, tarif d'adhésion) se modifie **directement sur GitHub**. Pages CMS ne gère que les actualités.

Cette section décrit la manipulation à la main. Si le code vous rebute, ou si la modification est d'ampleur, **la section 5 explique comment la faire réaliser par un assistant IA** — c'est ainsi que le site a été construit.

### Comment modifier un fichier sur GitHub

1. Aller sur **https://github.com/apic-parents/apic-parents-site**
2. Cliquer sur le nom du fichier à modifier.
3. Cliquer sur l'**icône crayon** (« Edit this file ») en haut à droite.
4. Faire les modifications dans la zone de texte.
5. Descendre et cliquer sur le bouton vert **« Commit changes »**, puis confirmer.
6. Le site se met à jour tout seul en une à deux minutes.

> **Conseil :** dans la petite case « Commit message », écrivez en une ligne ce que vous avez changé (« correction mail Les Chalets »). Cela constitue un historique précieux — et GitHub garde **toutes** les versions précédentes, donc **une erreur est toujours réparable** (voir section 9).

### À quoi correspond chaque fichier

| Fichier | Ce qu'il contient |
|---|---|
| `index.html` | **La page d'accueil.** Le grand titre, les chiffres clés (12 €, 6 établissements, depuis 1989), le bloc « Qui sommes-nous », la liste des établissements, les quatre encadrés « Ce que nous faisons », et les **6 actualités les plus récentes**. |
| `actualites.html` | La page qui liste **toutes** les actualités, sans limite de nombre. C'est la cible du lien « Toutes les actualités » de la page d'accueil. Elle se remplit toute seule : il n'y a jamais rien à y modifier. |
| `mentions-legales.html` | **Les mentions légales, obligatoires par la loi.** Accessibles depuis le pied de page. Elles nomment la directrice ou le directeur de la publication — le président ou la présidente en exercice. **À corriger impérativement à chaque changement de présidence**, ainsi qu'en cas de changement de siège social ou d'hébergeur. Leur absence est pénalement sanctionnée. |
| `college-michelet.html` | La page du collège Michelet : texte, contact mail, adresse, téléphone, lien vers le site du collège. |
| `college-fermat.html` | Idem pour le collège Fermat. |
| `college-les-chalets.html` | Idem pour le collège Les Chalets. |
| `lycee-fermat.html` | Idem pour le lycée Fermat. |
| `ecole-maternelle-lakanal.html` | Idem pour l'école maternelle Lakanal. |
| `ecole-elementaire-lakanal.html` | Idem pour l'école élémentaire Lakanal. |
| `_layouts/default.html` | **L'habillage commun à toutes les pages** : le bandeau du haut avec le logo et le menu, le pied de page, **et toute la mise en forme** (couleurs, polices, tailles). |
| `_layouts/post.html` | La mise en page d'un article d'actualité. |
| `_posts/` | Le dossier des actualités. **Normalement, on n'y touche pas à la main : on passe par Pages CMS.** |
| `assets/` | Les images : le logo, les photos ou illustrations des six établissements. |
| `assets/accueil.jpg` | **Actuellement inutilisé.** La page d'accueil affiche simplement le logo. Le jour où l'association disposera d'une vraie photo ou d'une illustration d'accueil, elle prendra la place du logo — voir `index.html`, bloc `hero-mark`. |
| `assets/favicon.ico`, `favicon-32.png`, `apple-touch-icon.png` | La petite icône affichée dans l'onglet du navigateur, et celle qui apparaît si le site est ajouté à l'écran d'accueil d'un téléphone. |
| `assets/og-image.jpg` | **L'image de partage.** C'est elle qui s'affiche quand quelqu'un colle le lien du site sur WhatsApp, Facebook ou dans un mail. Sans elle, les applications récupèrent la minuscule icône d'onglet et l'agrandissent : le résultat est très flou. |
| `assets/uploads/` | Les images et PDF envoyés depuis Pages CMS. |
| `_config.yml` | Les réglages généraux du site (titre, description). **À ne modifier qu'en connaissance de cause** — voir l'avertissement en section 7. |
| `.pages.yml` | Le réglage de Pages CMS : la liste des champs d'un article et la liste déroulante des établissements. |

### Cas concrets

**Changer une adresse mail de contact ou un numéro de téléphone**
→ Ouvrir la page de l'établissement concerné, chercher l'adresse, la remplacer. Attention : elle apparaît souvent deux fois, dans `mailto:...` et dans le texte affiché juste après. **Modifiez bien les deux.**

**Changer le tarif de l'adhésion ou le lien HelloAsso**
→ Le lien HelloAsso et le tarif figurent à **plusieurs endroits** : dans `index.html` (bouton du haut et ligne « 12 € par an et par famille »), dans `_layouts/default.html` (bouton « Adhérer » du bandeau, présent sur toutes les pages), et dans **chacune des six pages d'établissement**. Pensez à tout passer en revue. Un moyen simple de n'en oublier aucun : utiliser la loupe de recherche de GitHub sur `helloasso`.

**Remplacer une photo**
→ Le plus simple est de garder exactement le même nom de fichier : sur GitHub, ouvrir le dossier `assets`, puis **« Add file » › « Upload files »**, et déposer la nouvelle image avec le même nom. Elle remplacera l'ancienne, et aucune page n'est à modifier. Format conseillé : JPEG, largeur d'environ 1200 pixels, moins de 300 Ko.

**Changer le texte d'accueil ou les encadrés « Ce que nous faisons »**
→ Dans `index.html`.

**Changer une couleur ou la mise en forme**
→ Dans `_layouts/default.html`, tout en haut, entre `<style>` et `</style>`. Le rose de l'association est le code `#E11A7E`. C'est la partie la plus technique du site : à confier de préférence à quelqu'un d'à l'aise, ou à refaire faire.

---

## 5. Se faire aider par une intelligence artificielle

Le site a été conçu avec l'aide d'un assistant IA (**Claude Code**), et c'est la façon la plus simple de faire réaliser une modification qui dépasse l'écriture d'une actualité : refondre un texte, ajouter une section, changer une couleur, créer une nouvelle page.

> **Attention à ne pas confondre.** Un assistant IA ouvert dans un navigateur (ChatGPT, Claude sur claude.ai…) ne peut **pas** accéder aux fichiers de votre ordinateur : il pourra vous conseiller, mais pas modifier le site. Il faut un outil **installé sur l'ordinateur**, comme Claude Code, qui a accès au dossier.

### Comment cela se passe concrètement

1. Une copie complète du site est conservée sur l'ordinateur, dans **`Dropbox › College Michelet › APIC › Site web APIC`**.
2. Vous expliquez à l'IA ce que vous voulez changer. Elle modifie les fichiers **dans ce dossier**, sur l'ordinateur — le site en ligne n'est pas touché.
3. Vous relisez les modifications, et vous lui demandez la **liste des fichiers modifiés**.
4. Vous déposez ces fichiers sur GitHub : **« Add file » › « Upload files »**, glisser-déposer, puis **« Commit changes »**.
5. Le site se met à jour tout seul en une à deux minutes.

L'IA prépare donc le travail, mais **c'est vous qui publiez**. Rien ne part en ligne sans votre geste.

### La règle d'or : partir de la version en ligne

Le dossier de l'ordinateur **prend du retard** sur le site. C'est normal : les actualités écrites dans Pages CMS n'existent qu'en ligne, elles ne redescendent jamais toutes seules sur l'ordinateur.

Avant une séance de modifications, prenez donc une minute pour repartir du bon pied : sur le dépôt GitHub, bouton vert **« Code » › « Download ZIP »**, et remplacez le contenu du dossier par cette version fraîche.

Et surtout, au moment de publier : **ne déposez que les fichiers réellement modifiés**, jamais le dossier entier. Déposer un vieux dossier `_posts` ne supprimerait pas les articles récents, mais écraserait par des versions périmées les corrections faites entre-temps dans Pages CMS.

### Quoi dire à l'IA en début de séance

Le plus efficace est de commencer par la mettre en contexte. Vous pouvez copier-coller ce message tel quel :

> Le site internet de l'APIC se trouve dans ce dossier. C'est un site Jekyll publié sur GitHub Pages à l'adresse https://apic-parents.github.io/apic-parents-site/ — compte GitHub `apic-parents`, dépôt `apic-parents-site`. Commence par lire le fichier `GUIDE-DU-SITE.md`, qui explique comment le site est organisé et à quoi sert chaque fichier. Ensuite, je voudrais que tu… *(votre demande)*
>
> Quand tu auras terminé, donne-moi la liste des fichiers que tu as modifiés, pour que je sache lesquels déposer sur GitHub.

Ce guide sert alors de mode d'emploi à l'IA autant qu'à vous : elle y trouve la structure du site, les pièges, et les règles à respecter.

### Les précautions à prendre

- **Ne collez jamais de mot de passe** dans une conversation avec une IA — ni celui de GitHub, ni aucun autre. Elle n'en a pas besoin : c'est vous qui vous connectez pour publier.
- **Ne lui confiez aucune donnée personnelle** de familles ou d'élèves (listes, coordonnées, situations individuelles). Rappelez-vous que le dépôt est public.
- **Relisez systématiquement ce qui est factuel** : adresses, adresses mail, numéros de téléphone, dates, montants, noms. Une IA rédige bien, mais elle peut se tromper avec aplomb — ces éléments-là, vérifiez-les vous-même.
- **Signalez-lui ce qui se répète.** Le lien HelloAsso et le tarif d'adhésion figurent dans une dizaine d'endroits différents ; demandez explicitement qu'elle les traite tous.
- **Faites une modification à la fois.** Il est bien plus facile de revenir en arrière sur un changement isolé que sur une refonte complète.

### Une variante plus directe, pour qui est à l'aise

Le dossier de l'ordinateur peut être **relié directement au dépôt GitHub** (par un outil appelé *git*). L'IA peut alors publier elle-même, sans passer par le navigateur, et la copie locale reste toujours synchronisée — ce qui supprime d'un coup le problème de retard décrit plus haut.

C'est plus confortable au quotidien, mais cela suppose de mémoriser un accès GitHub sur l'ordinateur. Le dépôt par glisser-déposer, lui, fonctionne depuis n'importe quel ordinateur et ne laisse aucune trace : c'est pour cette raison qu'il reste la méthode décrite par défaut dans ce guide. Si vous voulez mettre en place la première solution, demandez-le simplement à l'IA.

---

## 6. Ajouter un nouvel établissement

Si l'APIC s'étend à un nouvel établissement, il y a **quatre** endroits à modifier — c'est le seul cas où l'on ne peut pas en oublier un sans casser quelque chose :

1. **Créer la page.** Le plus sûr : ouvrir une page existante proche (par exemple `college-michelet.html`), copier tout son contenu, puis sur GitHub faire **« Add file » › « Create new file »**, nommer le fichier (par exemple `college-untel.html`), coller, et adapter le texte. Dans les premières lignes, bien modifier `title`, `permalink` et `etab`.
2. **Ajouter la photo** dans le dossier `assets`, et corriger le nom de l'image dans la nouvelle page.
3. **Ajouter le lien** dans `index.html`, dans la section « Nos établissements ».
4. **Ajouter le nom** dans la liste déroulante de `.pages.yml`, pour pouvoir ensuite lui attribuer des actualités.

> **Le nom doit être rigoureusement identique** — accents et majuscules compris — entre le champ `etab:` de la page (étape 1) et la liste de `.pages.yml` (étape 4). C'est ce qui permet aux articles de se ranger tout seuls sur la bonne page. Une différence, même d'un accent, et la page restera vide d'actualités.

---

## 7. Les points de vigilance

**Ne pas renommer le dépôt GitHub.**
L'adresse du site contient le nom du dépôt (`apic-parents-site`). Ce nom est aussi inscrit dans le fichier `_config.yml`, à la ligne `baseurl`. Si l'un change sans l'autre, **le site s'affiche sans mise en forme et toutes les images disparaissent**. Si vous devez vraiment renommer, changez les deux en même temps.

**Les deux lignes d'adresse de `_config.yml` vont par paire.**
`url` contient le nom du serveur (`https://apic-parents.github.io`) et `baseurl` le sous-dossier (`/apic-parents-site`). La première sert aux aperçus de partage sur WhatsApp et les réseaux sociaux, la seconde à tous les liens internes du site. **Si l'adresse du site change un jour — voir la section 10 — il faut corriger les deux.**

**Ne pas supprimer le compte GitHub `apic-parents`.**
Le site disparaîtrait avec lui.

**Le dépôt est public.**
Tout ce qui y est déposé est visible par n'importe qui sur internet. **N'y mettez jamais de mot de passe, de liste d'adhérents, de coordonnées de familles, de RIB ou de document interne.** Les PDF déposés comme pièces jointes d'un article sont, eux aussi, publics — ce qui est normal pour un compte rendu, mais à éviter pour tout ce qui touche à des données personnelles.

**Les fichiers commençant par `_` ou `.` sont structurants.**
`_config.yml`, `_layouts`, `.pages.yml` : leur suppression casse le site. Les articles, eux, sont sans danger.

---

## 8. Les accès à transmettre au successeur

Ce guide étant public, **aucun identifiant n'y figure**. Les accès sont conservés à part, dans le fichier :

> `Dropbox › College Michelet › APIC › ACCES-SITE-APIC.md`
> *(volontairement rangé en dehors du dossier du site, pour qu'il ne puisse pas être mis en ligne par mégarde)*

Ce qu'il faut transmettre en main propre au moment de la passation :

- **Le compte GitHub `apic-parents`** — identifiant et mot de passe. C'est l'accès essentiel : il commande le site.
- **La boîte mail `apic31@gmail.com`** — elle sert aussi de porte d'entrée à GitHub (connexion via Google) et à la récupération de mot de passe. Sans elle, un mot de passe GitHub perdu est difficile à récupérer.
- **Le compte HelloAsso** de l'association, pour les adhésions.
- **Les boîtes mail par établissement** : `apic.michelet@gmail.com`, `apic.leschalets@gmail.com`, `apic.collegefermat@gmail.com`, `apic.lyceefermat@gmail.com`, `apic.maternelle.lakanal@gmail.com`, `apic.primaire.lakanal@gmail.com`.

Pages CMS n'a pas de compte propre : on s'y connecte avec le compte GitHub.

> **Recommandations pour la passation :**
> - Changer le mot de passe GitHub à chaque changement de président, comme on rend les clés d'un local.
> - Vérifier que l'adresse de récupération du compte GitHub est bien `apic31@gmail.com`, et que la nouvelle équipe y a accès.
> - Si l'authentification à deux facteurs est activée sur GitHub, **penser à transmettre les codes de secours** : sans eux, le compte devient inaccessible même avec le bon mot de passe. C'est la première cause de perte d'un site associatif.

---

## 9. En cas de problème

**Le site ne se met pas à jour**
Patientez deux ou trois minutes et rechargez la page en forçant l'actualisation (`Ctrl` + `F5`). Si rien ne change, allez sur le dépôt GitHub, onglet **« Actions »** : la dernière ligne indique si la reconstruction a réussi (coche verte) ou échoué (croix rouge). Une croix rouge signale presque toujours une faute de frappe dans un fichier récemment modifié.

**Une page s'affiche sans mise en forme, ou une image manque**
C'est le symptôme typique d'un problème de `baseurl` : voir la section 7.

**Une page d'établissement n'affiche aucune actualité**
Le nom de l'établissement ne correspond pas exactement entre l'article et la page : voir la section 6.

**J'ai fait une bêtise et je veux revenir en arrière**
Rien n'est perdu, GitHub conserve l'intégralité de l'historique. Ouvrez le fichier concerné et cliquez sur **« History »** en haut à droite : vous voyez toutes les versions précédentes. Ouvrez celle qui allait bien, cliquez sur les **« … »** puis **« View file »**, copiez le contenu, et recollez-le dans le fichier actuel.

**Une actualité n'apparaît pas**
Vérifiez sa date : les articles s'affichent du plus récent au plus ancien, un article ancien se retrouve donc en bas de liste.

---

## 10. Si vous voulez aller plus loin

Deux évolutions possibles, si un jour l'association le souhaite :

- **Basculer l'adresse `apic31.fr` vers ce site.** L'association possède déjà ce nom de domaine, mais il pointe aujourd'hui vers l'ancien blog Overblog. On peut le faire pointer vers ce site-ci : l'adresse deviendrait simplement `apic31.fr`, bien plus facile à communiquer aux familles que `apic-parents.github.io/apic-parents-site`. Cela se règle chez le fournisseur du nom de domaine, puis dans les réglages GitHub Pages — **sans oublier de corriger `url` et `baseurl` dans `_config.yml`** (voir section 7) — et l'hébergement reste gratuit. **Tant que ce n'est pas fait, deux sites de l'APIC coexistent en ligne** — c'est le point à trancher en priorité, car les parents qui cherchent l'association tombent d'abord sur l'ancien.
- **Une copie de sauvegarde.** Le site vit sur GitHub, mais il est prudent d'en garder une copie hors ligne. Sur la page du dépôt, bouton vert **« Code » › « Download ZIP »** : vous obtenez l'intégralité du site en un fichier. À faire une fois par an, et à ranger dans le Dropbox de l'association.

---

*Guide rédigé le 27 août 2026. Si le site évolue, pensez à mettre ce fichier à jour : c'est lui qui permettra à la personne suivante de prendre la suite sereinement.*

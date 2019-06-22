# DOSSIER RNCP - Thomas De Queiros - 2019
# FLOW - Social Network
## SOMMAIRE
1. Liste des compétences du projet
2. Resumé en anglais du projet
3. Cahier des charges
4. Gestion de projet
5. Specifications fonctionnelles
6. Specifications techniques
7. Réalisations
8. Veille et recherches

# Liste des compétences du projet

Le projet présenté dans le cadre de ce dossier couvre les compétences suivantes :
- Réalisation d'une maquette pour l'application
- Développement de composants d'accès aux données
- Développement d'une partie front-end d'une interface utilisateur web
- Développement d'une partie back-end d'une interface utilisateur web
- Conception d'une une base de données
- Mise en place d'une base de données
- Collaboration à la gestion d'un projet informatique et à l'organisation de l'environnement de développement
- Concevoir et développer une application mobile

# Résumé du projet

The project consists in developing the social network of tomorrow.
 Following the observation of the social networking market, my associates and I have highlighted the growing development of the use of voice as a means of communication, especially among young people. However, it so happens that among the large networks currently occupying the first places in the various stores, none of them offers the sharing of voice only posts. This is why we decided to develop, initially in the form of an application, the first exclusively vocal social network, allowing the sharing of audio excerpts of up to fifteen seconds, pushing users' creativity as Vine was able to do a few years ago, called **FLOW**. 
The application will first be offered on Android before being quickly adapted for iOS. To do this we use Cordova, a solution that allows the development of cross-platform applications from the same code base. In addition, we use web technologies to design the front end of our application, allowing us to quickly test and easily obtain the desired look and feel through our expertise in web technologies.
The team behind this project consists of five developers including myself, computer science students in the same class. The idea was born a year and a half ago, we were then 2 people. Several months after taking the time to carefully write a solid specification, 3 additional developers joined us to form the team we are today.

# Cahier des charges

Le cahier des charges du projet a été élaboré au commencement de ce dernier. L'idée étant née il y a un an et demi par deux des membres de l'équipe actuelle, un associé et moi même, il a fallu l'étayer durant plusieurs mois avant d'entamer le développement du projet d'un point de vue technique.
Ce cahier des charges est par ailleurs encore aujourd'hui amené a régulièrement évoluer.
Afin de faciliter son édition mais aussi son évolution et son accès par les différents membres de l'équipe, il a été mis en place dès le début du projet, un google docs partagé en ligne. Ce dernier contient pour chaque entrée, la date de cette dernière, et le contenu ajouté au cahier. Il peut aller de la définition de fonctionnalité, à la modification de fonctionnalités déjà définies en passant par des spécifications techniques à prévoir en amont.
C'est dans ce cahier qu'a été définis le nom de l'application mais aussi ses fonctionnalités principales, dans un premier temps pour les utilisateurs, puis dans un second temps pour l'équipe de développement afin d'anticiper coté serveur comment seront gérées nos données.

Extraits du Cahier des Charges :
```text
02/10/2017

Recherche de noms :
Few Twelve Flap Blee Jam Wive Flive
Nom retenu : FLOW

Temps des Flows : 12 secondes


06/10/2017

Fonctionnalités :
Enregistrer un flow et le partager directement
Consulter des flows :
- Son flux perso
- Catégories (à définir plus tard ex : top / rap / jokes)

Mon profil :

- Mes flows (possibilité de voir le nombre de likes et les commentaires)
- Mon activité (regroupant mes likes et mes partages triés 
  par date + couleur différente)
- Mon nombre de flowers (personne abonnés à mon activité)
- Score de notoriété

Messages privés :

- Envoyer texte ou audio (priorité à l’audio)
- Audio tj limité à 12 sec

Partage :

- Choix : Public / Mes flowers / Flowers spécifiques (cocher les 
  noms + barre de recherche)

Informations générales :

Commentaires :

- audio ou texte
- audio pas plus de 5 sec (à définir)
- commentaire peuvent être likées pour définir top coms
- 2 catégories de commentaire affichables (2 modes en gros)
- commentaires audio par défaut
- 3 Hashtags par flow pour la recherche
- Création de catégories auto regroupant les flows en fonctions 
  de leurs Hashtags (ex : Flow / Battles / Rap => Catégorie Rap)
- Top 50 : En fonction du nombre de likes par jour, place dans le 
  top affiché sur les flows (ex : numéro 2 des tendances)


09/10/2017

Interface :

- Sticky button en bas de l’écran pour pouvoir enregistrer un 
  flow à tout moment
- Home : mon flux perso
- Discover avec les catégories et tops Flows
- Onglet notifications
- Onglet mon profil

Sticky button :

-   Placé au centre en bas en gros.
-   Single tap => attend un autre tap pour s’arrêter
-   Long press => stop quand on lache
-   Options : annuler, écouter, choisir l’audience 
    (public / mes flowers / spécifique),
-   Hashtags : FACULTATIFS à cocher, quelques hashtags 
    proposés (en fonction des tendances si premier flow, mix 
    tendances et mes précédents hashtags) + possibilité d’en ajouter 
    avec un bouton ”+”
-   A la fin de l’enregistrement popup demandant le titre du flow
   
Home :

-   Défilement vertical
-   Contenu du bloc : Photo de la personne, nom, titre du flow,
    like, comment
    
Discover :

-   Défilement horizontal
-   Chaque catégorie est un top journalier 
    (même système que top 50) regroupant les Hashtags de la catégorie
-   Contenu du bloc : Photo de la personne, nom, titre 
    du flow, like, comment, flow l’auteur
    
Notifications :

-   Liste des notifs
    
Mon profil :

-   Mon Nom (can edit)
-   Ma Photo (can edit)
-   Nombre de Flowers -> Vue Conversations -> onglet liste de 
    tous les flowers triées de A à Z
-   Temps cumulé total des écoutes de tout tes flows (realtime update ?)
-   Sous Onglet : Mon activité -> liste par blocs de mon 
    activité ce que j’ai aimé, partagé, posté
-   Mes Flows : écran scindé en 2 :
-   Partie supérieure : Défilement horizontal de mes 
    flows les plus populaires
-   Partie inférieure : Défilement vertical de tous mes flows 
    (triable par date ou likes)
    
Disposition des onglets : Home | Discovery | Profil | Notifications

  
17/10/2017

Trois options : Like / Echo (=partage) / Comment

La timeline est composée de tous les Échos de nos flowers, et 
complétée par leurs likes

ex : la timeline est composée de 50 éléments, il y a eu 30 echos 
depuis votre dernière connexion, la timeline sera composée 
des 30 echos, puis complétée par 20 likes random de vos flowers, 
le tout trié par date.

  
18/10/2017

Dans l’écran Timeline, tapoter une div l'agrandit, montrant les 
commentaires des nos flowers en premiers, mis en valeurs graphiquement, 
puis les top commentaires (les plus likés).

Si on appuie sur l'icône de commentaire, ça agrandit également la div, 
mais ça amène directement l’utilisateur à focus sur l’input pour 
rédiger un commentaire.


19/10/2017

Contenu d’une div agrandie sur la timeline :

-   Commentaires des nos flowers
-   Top Commentaires
-   Bouton pour like un commentaire 
-   Like / Echo / Comment buttons 
-   Input pour commenter
    

06/11/2017

Au premier lancement , demander la permission d'accéder au 
contacts et proposer d’ajouter des amis en fonction 
de la liste de contacts.


04/12/2017

Pour l’affichage des catégories (acapella, rap, drunk etc....) 
on affiche le dégradé comme pour l’affichage du top 50, mais 
au lieu d’afficher les numéros de chaque flow (1, 2, 3 etc…) 
on affiche le nom de la personne comme pour l’affichage de la 
page d’accueil.


08/12/2017

Ajouter un effet de “pulse” au bouton de record de flow 
lors de l'écriture d’un new message
  

15/12/2017

Faire page d’inscription et de connexion.

Activé regroupe une liste de flow avec en icône les actions 
réalisées par le détenteur du profil

Flow regroupe la liste des flows posté par l’utilisateur

Flowers affiche une liste d’utilisateurs avec l’image , le nom,
 un bouton permettant de flow la personne ainsi qu’une liste 
 alphabétique style android ainsi qu’une barre de recherche

Flowings affiche une liste d’utilisateur avec l’image , le nom,
 un bouton pour unflow , liste alphabétique , barre de recherche.

Profil utilisateur contient un bouton pour flow où unflow 
ainsi que la possibilité d’envoyer un message à l’utilisateur.

  
20/12/2017

Dans l’onglet activitée de mon compte lorsque la personne a 
commenté un FLOW lors de l’appui sur la div , le commentaire 
de la personne est pin (epinglé en top).


22/12/2017

Définir précisément le type d’utilisateur que l’on veut cibler

  
15/01/2018

Ajouter glow effect sur les curves du bouton flow partout dans 
l’interface et sur l’icône de l’application.

RECORD de FLOW

-bouton réécouter
-bouton delete
-bouton

RECORD de FLOW PANEL 2

-bouton croix à droite du titre du flow lors de l'édition 
permettant de delete tout d’un coup

 
22/01/2018

Pseudo unique par utilisateur, pas de nom et prénom affichés.
faire connection mail.

  
05/02/2018

Pseudo unique par utilisateur, pas de nom et prénom affichés.

Choix BETA : non
  

01/03/2018

Modification du design suite au critiques de Team TO :
top 50 : remplacement de dégradé par notre nuancier → voir 50shadesofFLOW
discover panel : voir si remplacer dégradé par shades


23/05/2018

Arrivée de Victor , gérer le système de notification : 
possibilité de recevoir les notifications de ses flowing uniquement.


28/05/2018

Définition des design/choix de dev/développement . version 3.0 
du design et premier test de record de flow.

 
30/05/2018

implémentation des story dans flow :
- story éphémères ( comme snap )
-interface similaire à instagram
-une couleur différente par flow qui compose une story
-pas d’image , titre optionnel
-possibilité de commenter les story
-système de swipe

possibilité de répondre au commentaire par audio

  
15/06/2018

Après record d’un flow 3 choix :
-private
-public
-stories


15/10/2018

Panel pour affichage d’un flow particulier, lorsque 
l’on clique sur une notification concernant un flow→ exemple 
je clique sur “ chris liked this flow” ouvrant en fullscreen 
le flow concerné

interface commentaire : interface qui pup du bas de l'écran comme Tik Tok

panel insight : stats des impressions du flow
story : ajouter le nombre de personnes ayant vu la story

  
23/10/2018

Migration de HacknPlan vers ASANA

Affichage d’un bouton de stats du flow dans le petit onglet settings .

Lorsque que l’on est identifier sur un commentaire, 
mettre ce commentaire tout en haut de la liste 
(haut dessus du top commentaire).

  
29/10/2018

Mettre “You” lorsque l’on consulte son propre flow 
depuis un autre profil


29/01/2019

Redesigner la page de customisation de son flow

retirer les backgrounds par défaut, mettre par défaut une image 
abstraite en fond et avoir seulement deux boutons PRENDRE UNE PHOTO 
ou SELECTIONNER UNE PHOTO et avec la place restante garder 
le design de choix avec scroll mais pour selectionner 
des filtres audio (style bubbly)
```

Au travers de ces différents extraits, différentes spécifications à la fois fonctionnelles et techniques se distinguent. Contrairement à un cahier des charges plus classiques, une notion de temporalité permet également de suivre l'historique des différents changements et les raisons de ces modifications.

En parallèle de l'élaboration du cahier des charges, nous avons également conçu différentes maquettes particulièrement détaillées de l'application, des différents panels et des interactions possibles dans celle-ci. Nous détaillerons ces maquettes dans la partie réalisation de ce dossier.

# Gestion de projet
## Gestion des tâches
La gestion du projet est un élément central définissant notre manière de travailler. Nous sommes passé par différentes étapes et différents outils dans la gestion du developpement de FLOW. 

Dans un premier temps, notre outil principal était le document google docs hébergé en ligne permettant de partager nos idées, nos besoins et notre avancement dans la définition des besoins et des tâches à faire. Néanmoins ce système a très vite vu ses limites notamment dès que nous avons été plus nombreux à rejoindre l'équipe mais aussi lorsque le développement technique a commencé.

Le premier outil que nous avons utilisé a été hacknplan. Cet outil en ligne propose l'assignation de tâche à une personne, la répartition de ces dernières et leur catégorisation (Design, Développement, Marketing, etc...).

![test](https://i.imgur.com/dclkZCi.png)*HacknPlan Dashboard* 

Cet outil, bien que pratique, a rapidement montré ses limites. En effet, ce dernier s'adresse plutôt à un certain type de projet bien défini (en l'occurence le developpement de jeu vidéo) assez éloigné de notre besoin. De plus certaines fonctionnalités nous faisant défaut, nous avons été amené à chercher une alternative à ce dernier.
Nous avons alors benchmarker différentes solution dont **Asana**, un concurrent similaire à **HacknPlan** proposant une interface plus intuitive et plus professionnelle malheureusement l'application web s'est retrouvé être assez gourmande en ressources et nous avons pu rencontré divers ralentissements réguliers.

![](https://luna1.co/764fe7.png) *Asana*

L'outil que nous avons finalement retenu, **ClickUp** nous as séduit pour différentes raisons. Dans un premier temps, il propose une interface claire, épurée et moderne, facilitant la productivité contrairement à l'interface assez datée et fouillis de HacknPlan. Dans un second temps, il propose de nombreuses fonctionnalités supplémentaires très utiles comme les sous-tâches, l'historique de chaque tâche, leur suivi, l'intégration d'un bloc note.
De plus, **ClickUp** propose une extension pour navigateur permettant de toujours garder un œil sur nos besoins en un coup d’œil, mais l'outil propose également une application lourde, pour des performances maximales sur ordinateur, ainsi qu'une version mobile nous permettant de toujours rester à jour sur les tâches assignées à chacun.

![](https://clickup.com/images/pricing/platforms@2x.png)
*ClickUp*

Pour créer et assigner ces tâches, nous organisons des réunions de groupe une à deux fois par semaine pour définir les tâches les plus urgentes, quelle personne y est assignée et quelle échéance est attribuée à celle-ci.
Je suis généralement celui qui distribue et répartit les tâches entre les différents membres du groupe bien qu'il n'y ait pas de chef de projet à proprement parler et que chaque membre à autant de pouvoir que les autres. Il n'existe pas de hiérarchie entre les développeurs.

## Gestion des fichiers

Afin de travailler à plusieurs sur le même projet, nous avons choisi de mettre en place un **git** permettant de gérer à la fois nos versions mais aussi de scinder nos fonctionnalités en différentes branches.

Le projet dispose de deux parties. La partie front-end et la partie back-end. Nous sommes quatre développeurs dont moi même à travailler principalement sur la partie front-end, et un développeur à travailler majoritairement sur la partie back-end. Néanmoins pour l'ajout de chaque fonctionnalités nous implémentons celle-ci en front et en back, nous permettant de maîtriser l'architecture du projet de bout en bout.

Deux repository sont disponibles, un pour la partie serveur, et un pour l'application mobile en front. Nous gérons nos push, commit et merge à l'aide de l'outil **Github Desktop** proposant une interface très complète et bien plus pratique pour la résolution de conflits et l'historisation que l'interface en ligne de commande.

![enter image description here](https://i.imgur.com/7Kdseah.png)
*GitHub Desktop*

Ces outils constituent notre manière de gérer le projet, une planification des tâches au travers de ClickUp, et une gestion des environnements de développement au travers de différentes branches à l'aide d'un git, gérer avec le client GitHub Desktop.

# Spécifications fonctionnelles

Différentes actions doivent être possibles au sein de l'application. La plus importante étant la publication d'audio. Ces posts sont appelés *flows* et ont une durée maximale de 15 secondes.
Un utilisateur doit pouvoir accèder a du contenu dès le lancement de l'application avant même de creer son compte. Si l'utilisateur essaye de faire une interactions nécessitant un comtpe (comme liker un flow, ou poster un commentaire par exemple) alors une popup non intrusive apparait lui proposant de se connecter avec tous les réseaux sociaux les plus utilisés : 
- Facebook
- Google
- Instagram
- Twitter

Mise en place d'un système de stories, permettant aux utilisateur de poster un story de purement audio de 15 secondes disponible uniquement 24 heures pour les abonnés de l'utilisateur.
Le système d'abonnements justement est similaire à celui de Twitter ou instagram, il est possible de s'abonner aux utilisateurs dont le contenu nous plait, les publications de ces derniers apparaitront alors dans notre fil d'actualité et nous auront accès à ses stories.
Lors de la publication d'un flow, il est possible d'ajouter une image de fond au flow, ainsi qu'un titre et une description. Un système de hashtag permettant de catégoriser un flow est également à mettre en place.

Mettre en place un onglet Explore permettant de rechercher parmis les flows et les comptes de différents utilisateurs. Permettre également d'explorer les meilleurs flows par catégorie (Musique, Politique, Humour, etc...) et créer une catégorie particulière : TOP 50 mettant en avant les flows les plus populaires du moment.

Mettre en place un onglet de messagerie privée permettant de discuter par écrit et par vocal avec des utilisateurs.

Enfin, mettre en place un système de notification à la fois dans l'application et en dehors (à la manière de ce que font des concurrents comme Twitter). 
Evidemment les flows doivent pouvoir être liké, partagés et commentés.
Dans un premier temps ces commentaires seront purement textuels, contrairement aux stories dont les réactions sont uniquement vocales.

Pour le partage, un flow doit pouvoir être partagé en dehors de l'application. Un appui sur le bouton partage doit générer un lien, quand un utilisateur clique sur le lien, si celui-ci à l'application FLOW installé, l'application ouvre le flow en question dans l'app, si non un player web permet de lire le flow dans un navigateur invitant par la suite l'utilisateur à installer l'application sur son téléphone.

# Spécifications techniques

Les spécification techniques de l'application sont multiples. Elle doit être disponible sur iOS et Android, ainsi, dans un soucis de continuité du code et facilité de maintenabilité, nous décidons de developper une application cross-platform hybride réalisée avec Cordova.
Cordova est un framework permettant d'utiliser les developpement web pour réaliser des applications hybrides utilisant des fonctionnalités natives sur mobile sur iOS et Android. 

Le coeur de notre application reposant sur l'enregistrement audio, nous nous devons de garantir une qualité maximale tout en limitant au mieux le poids des fichiers générés. Pour répondre à ce besoin, nous optons pour un codec audio open source récent de dernière génération garantissant une qualité maximale pour une taille de fichier tout à fait acceptable : OPUS.
Ce codec est le même utilisé par whatsapp néanmoins, en jouant avec le bitrate de l'audio capturé, nous pouvons trouver un juste milieu entre qualité et poids du fichier audio généré pour devancer ces derniers en terme de qualité tout en garantissant un stockage optimal.
Coté client, nous utilisons différentes librairies pour faciliter le développement. Jquery est une libraire permettant notamment de faire des appels AJAX à notre api. Cette librairie nous permet également de gérer nos divers evenements sur les éléments HTML de notre application. 
Framework7 est, comme son nom l'indique, un framework web pensé pour une utilisation front. Ce dernier permet en quelques lignes de code, de facilement intégré des éléments ressemblant à s'y méprendre à des éléments natifs pour Android et iOS à l'aide d'éléments web HTML et CSS au comportement dynamique géré en javascript. C'est grâce à cet outil que nous pouvons par exemple gérer facilement la navigation par swipe entre les différentes pages de l'application.

Coté serveur et infrastucture, nous optons pour une base de données MySQL avec une api en PHP que l'on requête en AJAX depuis notre application.
Au début du projet nous utilisons le même serveur pour la base de données, l'api, et le stockage d'images et de flows mais dans un futur proche, nous planifions un serveur différent pour le stockage de flows et d'images et un serveur pour la base de données et l'api. Le premier equipé d'un disque dur maximisant le stockage à la rapidité, le second équipé d'un SSD et d'un nombre de RAM élevé pour maximisé la rapidité.

# Réalisations
## Design
Les réalisations liées à ce projet sont nombreuses et bien qu'elles prennent au final principalement la forme d'une application mobile, le fonctionnement de cette dernière n'est que le résultat de multiples réalisations précédentes qui bout à bout forment FLOW.

Afin d'étayer les différentes productions liées à ce projet, une présentation chronologique de l'évolution de ce dernier m’apparaît judicieuse.

En effet, une fois le cahier des charges suffisamment détaillé pour une première ébauche, nous nous sommes attelés à la réalisation de maquette de design, une étape cruciale pour notre application tant nous savons l'esthethique, l'experience utilisateur et l'UI autant que l'UX primordial à la réalisation d'une application de qualité. Notre plus grande problématique a été en premier lieu de trouver comment un réseau social basé uniquement sur l'audio pouvait réussir à capter et retenir des utilisateurs qui pour la plupart seront issus d'une génération ayant grandi avec l'image et la vidéo comme support numéro un de médias sur internet.
De ce postulat est né un premier concept réalisé dans Photoshop, logiciel que je maîtrise assez bien pour réaliser ces premières planches en quelques temps. 

![](https://i.imgur.com/YM6nQlN.jpg)
![](https://imgur.com/d7OgcHL.jpg)
*Premiers concepts de l'application*

Ces premières planches nous ont permis de rapidement visualiser les différentes parties de l'application. L'ensembles des planches de cette première version est disponible en annexe de ce dossier.
Une fois toutes la parties principales de FLOW conçues, nous avons décidé de repasser sur le design général de l'application que nous avons produit. Insatisfait de la plupart de nos choix et poussés par les avis assez mitigés d'expert en design rencontrés sur nos lieux de travail respectif, nous avons décidé de donner naissance à une nouvelle version du design de notre réseau social, motivé par la volonté d'une interface plus pure, plus complète, à la charge cognitive plus faible et plus moderne dans son apparence.
Pour cela, étant chargé de la réalisation de ces maquettes, j'ai également fait évoluer mon outil en passant de Photoshop à Adobe XD, une logiciel spécialisé pour l'élaboration de maquettes me permettant dans un permier temps de travailler deux à trois fois plus rapidement puis dans un second temps m'ajoutant des fonctionnalités particulièrement bienvenues comme la possibilité de réaliser des maquettes interactives avec des transitions entre les différentes pages de l'application nous offrant un rendu des plus crédibles sur la direction que prend notre réseau.
Armé de ce nouvel outil et ayant en tête une vision bien plus précise de la direction à prendre pour la refonte de notre interface, j'ai pu réaliser les semaines qui suivirent la majorité des interfaces de l'application dans une version 2.0 du plus bel effet.

![](https://imgur.com/CTyzXBv.jpg)
![](https://imgur.com/ZoOs3ZX.jpg)
*Nouveaux concepts après re design de l'app*

Encore une fois, toutes les planches, et elles sont nombreuses, de le nouvelle version sont disponibles en annexe, l'évolution du design y est encore plus flagrante.

## Developpement Front-end

Une fois ces maquettes réalisées, le developpement concret de l'application a pu débuter. L'équipe s'est alors scindé en deux groupes, l'équipe chargée de poser les fondations de l'application en front (constituée de 4 developpeurs) et l'équipe chargée de mettre en place l'environnement de back pour notre serveur et notre api (constituée d'un developpeur).
J'ai personnellement participé à la réalisation front du squelette de notre application. C'est ici que l'utilisation de Framework7 entre en jeu puisque notre première étape a été la réalisation d'une SPA (Single Page Application) proposant de naviguer entre différents onglets correspondant aux différentes parties de l'application (Home, Explore, Messages, Notifications, etc...) à l'aide d'un système de swipe. Or Framework7 propose justement un pareil système qu'il a fallu adapter à Cordova pour pouvoir le porter dans une application android hybride.
Pour rappel Cordova est un framework proposant de réaliser des application android et iOS à partir de technologies web, c'est donc à partir de ce framework que nous travaillons en adaptant ainsi les librairies comme Framework7 pensées pour le web à notre application afin de rendre l'experience utilisateur la plus proche possible de celle d'une application native.
Cette première étape d'onglet dit "swipeable" nous a posé de nombreux problèmes. En effet, la dernière version disponible de Framework7 au moment où nous avons commencé à l'utiliser, la version 3.5, nous avons constaté un problème dans la mécanique de swipe proposée par la librairie. En effet, dans l'exemple proposé dans la documentation, cet effet utilise une autre librairie sous-jacente très populaire appelée Vue.js or nous voulion éviter d'utiliser un maximum de librairie afin de maitriser de bout en bout les fonctionnement de l'application tout en réduisant son poids au minimum. C'est pourquoi face à ce problème j'ai fais de nombreuses recherches pour tenter de le résoudre. La plupart du temps, ma manière de procéder lors de recherches de ce type est l'utilisation de Google avec lequel j'effectue systématique ma recherche en anglais afin de maximiser le nombre de résultats et améliorer la pertinence des réponses que j'obtiens. En général je privilégie les réponses du forum technique massivement populaire auprès des developpeurs qu'est [Stack Overflow](https://stackoverflow.com). Ce dernier propose des millions de réponses triées par pertinence et documentées régulièrement par des exemples et extraits de code accompagnés de capture d'écrans ou d'image explicites permettant la résolution rapide et efficace de son problème. La communauté derrière le site est à la fois immense et extrêmement réactive quand il s'agit d'aider une personne rencontrant un problème. Cela me permet de gagner du temps et donc en productivité lors de mes recherches. En plus ce forum, j'utilise systématiquement la documentation officielle des librairies que j'utilise que ça soit celle de Framework7 sur [Framework7.io](https://framework7.io/docs/) ou bien celle de [Cordova](https://cordova.apache.org/docs/fr/latest/guide/cli/).
Cette recherche m'a amené a identifier le problème et j'ai alors décidé d'utiliser la version précédente de Framework7, la version 1.7, utilisant une toute manière de fonctionner. Une fois ce changement effectué mon problème était résolu et j'ai pu construire notre premier prototype d'application fonctionnel.
L'écart de version de Framework7 s'explique par deux version majeures différentes, la v1 et la v2 donc les versions actuelles suivent l'architecture bien qu'actuellement en version 4.4.3 notre version utilise donc à l'inverse l'architecture v1, bien plus adaptée à nos besoins.

Cette première étape franchie, nous décidons d'opter pour un type d'application SPA.

### Différences entre SPA et MPA

Lorsque l'on parle d'application mobile et plus particulièrement d'application hybride reposant sur une architecture web, deux grande familles d'applications entrent en jeu. Les SPA pour Single Page Application et les MPA pour Multiple Pages Application. Leur nom est assez explicite, le premier type propose tout le contenu de l'application dans une seule et même page qui affichera ou cachera alors différents éléments en fonction du contexte, un système de vue est alors régulièrement utilisé pour simuler différentes pages dans une seule et même véritable page. Le second repose sur la navigation entre différentes pages à la manière d'un site plus classique. Chaque solution apporte son lot d'avantages et d'inconvénients et s'adapte à différents usages. Les raison pour lesquelles nous avons opté pour une SPA sont multiples. 
Tout d'abord, d'un point de vue purement esthétique, ce choix nous permet de contrôler entièrement les transitions entre les différents éléments de l'application. D'un point de vue technique ensuite, il est beaucoup plus facile pour nous de sélectionner quelle partie de l'application doit charger, quelle partie doit être cachée en attendant un événement particulier qui aurait été plus difficile à mettre en place avec une MPA où les informations doivent transiter d'une page à l'autre. Enfin, de par la nature de notre application, il est plus évident de stocker des informations récupérées en arrière plan dans un tel type d'application plutôt qu'en MPA.
Malgré tout, nous avons décidé d'utiliser quelques astuces s'apparentant au développement de MPA pour concilier les avantages de la SPA à ceux d'une MPA. En effet un des avantages d'une MPA est la lisibilité et la gestion claire des différentes pages d'une application puisque ces dernières sont séparées en différents fichiers. C'est pourquoi, à l'aide de JQuery, nous utilisons nous aussi différents fichiers correspondant à différentes pages, qui sont ensuite chargés dans une seule et même page, concevant ainsi notre SPA mais tout en conservant une scission entre nos différents fichiers. De cette manière le code est plus facile à maintenir, et à lire, évitant un seul et même long fichier de milliers de lignes dans lequel il est très difficile de s'y retrouver.


Une fois le squelette de notre SPA terminé, nous avons pu nous répartir les premières différentes tâches correspondant aux différentes fonctionnalités de FLOW. Pour ma part j'ai travailler sur l'enregistrement de fichier audio, dans un premier temps en local sur l'appareil, puis dans un second temps envoyé sur le serveur, nous verrons cette seconde partie dans la section back et communication api de ce dossier. 

---
### Enregistrement audio
Pour réaliser la fonctionnalité d'enregistrement audio, de nombreuses étapes ont été nécessaires. La première est l'interfaçage entre la brique web de l'application et la brique native propre à Android dans notre cas qu'il faut assembler par l'intermédiaire de Cordova. En effet, pour accéder aux capteurs natifs de l'appareil comme le microphone, qui est en l'occurence le coeur de cette fonctionnalité, il faut dans un premier temps importer un plugin permettant l'interfaçage entre le javascript, le langage dans lequel nous rédigeons notre projet, et la classe native à android en java gérant les divers paramètres et fonctions du micro. Heureusement, Cordova propose un plugin facilitant cette intégration. La seconde étape est particulièrement spécifique à Android. En effet, sur cette plateforme, il est impossible d'utiliser certaines fonctionnalités de l'appareil sans avoir obtenu les autorisations précises de l'utilisateur pour y accéder. Ce système est appeler le système de permissions et pour ne rien arranger, il est diffère à la fois d'une version d'Android à l'autre mais aussi d'un appareil à l'autre puisque sa manière de fonctionner est influencé par la surcouche Android propre à certains constructeurs. Par exemple sur mon appareil, un Vivo X21, les permissions sont par défaut refusées par l'appareil sans notifier l'utilisateur qui doit par lui même aller les activer dans les paramètres du téléphone à moins que l'application ne force la demande ce ces dernières contrairement au OnePlus d'un de mes collègues dont la surcouche OxygenOS va plus facilement proposer ou du moins notifier l'utilisateur des différentes permissions requises par l'application. Ces spécificités ont donc du être gérer par un système de demande de permissions que j'ai implémenté. Ainsi lorsque l'utilisateur appui sur le bouton d'enregistrement d'un FLOW, une fenêtre native d'Android demande à l'utilisateur si ce dernier souhaite donner la permission ou non à l'application d'utiliser son microphone. Cette permission est ensuite sauvegardée pour la prochaine utilisation et un message d'erreur s'affiche en cas de refus de cette dernière.
```javascript
// Record parameters
var  BitsPerSecondDefault  =  "12000";
var  soundClips  =  document.querySelector('.sounds-record');
var  chunks  = [];
var  mediaRecorder;

// Setup record environment
function  setup()  {
	// Keep screen awake during recording
	window.plugins.insomnia.keepAwake();
	
	// If recording is available
	if (navigator.mediaDevices  &&  navigator.mediaDevices.getUserMedia) {
		var  constraints  =  {
			audio:  true
		};
		
		chunks  = [];
		
		// Recording environment is all good, creating 
		// a recorder with custom parameters
		var  onSuccess  =  function  (stream)  {
			mediaRecorder  =  new  MediaRecorder(stream,  {
				audioBitsPerSecond:  BitsPerSecondDefault
			});
			
			// Recording ended, saving audio file
			mediaRecorder.onstop  =  function  (e)  {
				Save(mediaRecorder);
			}
			
			// Record data input, add to chunks
			mediaRecorder.ondataavailable  =  function  (e)  {
				chunks.push(e.data);
			}
			
			// Start recording
			mediaRecorder.start();
			// Update visual wave according to audio input
			wave(stream);
		}
		
		// Error occured during record setup
		var  onError  =  function  (err)  {
			alert("error : recording failed.");
			alert(err);
		}	
		
		// Access record device if available and return success or failure
		navigator.mediaDevices.getUserMedia(constraints)
			.then(onSuccess, onError);
		}  
	else  {
		alert("error : can't access media device");
	}
}
```
Cet extrait de code montre l'utilisation du microphone en javascript depuis une application cordova. Dans un premier temps, on vérifie si l'environnement d'enregistrement est disponible, si c'est le cas alors nous créons un *MediaRecorder* c'est à dire un objet javascript charger d'enregistrer de l'audio. Pour ce faire ce dernier creer un tableau de *chunks*. Des chunks sont des cours morceaux contenant des portions de données traduites depuis l'audio en données binaires. Une fois ces morceaux mis bout à bout nous pouvons reconstituer le fichier audio dans son ensemble. Une fois l'enregistrement lancé, le MediaRecorder écoute sur l'appareil *MediaDevice* disponible et transcrit bout par bout en temps réel l'audio qu'il ajoute dans le tableau *chunks*.

Lorsque l'enregistrement est terminé, un fichier binaire est alors généré, appelé blob ce dernier est alors converti dans le format de notre choix, en l'occurence un .opus, puis ce dernier est envoyé sur notre serveur.

```javascript
// Exemple de la fonction de sauvegarde d'audio
function  Save(mediaRecorder)  {
	blob  =  new  Blob(mediaRecorder.chunks,  {
		'type':  'audio/opus; codecs=opus'
	});
	mediaRecorder.chunks  = [];
	var  audioURL  =  window.URL.createObjectURL(blob);
}
```
Dans cet extrait on voit que le MediaRecorder précedement détaillé est envoyé en argument. Ce dernier nous permet de récuperer le tableau de chunks contenant nos données. On crée alors un blob, c'est à dire un objet binaire contenant les informations traduites des chunks en un seul et même fichier facilement convertissable derrière en mp3 ou dans notre exemple en opus. C'est ce que nous permet la fonction Blob prenant en argument nos chunks et le type de fichier désiré en sortie. Une fois notre blob crée, on reset notre tableau de chunks pour le prochain enregistrement, on obtient un path, c'est à dire un chemin d'accès, pour notre fichier recemment crée à l'aide de la fonction createObjectURL pour pouvoir faire référence à ce fichier et par la suite l'envoyer à notre serveur.

---

### Creation de blocs et lecteur audio

Pendant mon travail sur l'enregistrement audio, un de mes collègues a pu travailler sur la création des blocs pour nos flows. En effet, dans notre interface, nous avons fais le choix d'afficher un flow par un bloc regroupant toutes les informations du flow à savoir son titre, sa description, son auteur, sa date, la possibilité de l'aimer, le commenter, le partager et bien evidemment de le jouer. Pour ce faire nous avons conçu notre propre player audio.
En effet, j'ai étroitement collaborer avec mon collègue pour le concevoir, dans un premier temps nous avons essayé une librairie appelé Howler.js gérer la lecture de fichier audio avec un certain nombre de fonctionnalités intégrées mais très vite nous avons rencontré des soucis lorsque nous generions plusieurs players à la fois qui diffusaient de l'audio à tour de rôle de différents fichiers. C'est pourquoi dans un second temps nous avons opter pour une méthode nous offrons bien plus de contrôle, celle de gérer nous même notre player audio en le créant de toute pièce.
Pour cela, javascript nous offre toutes les fonctionnalités dont nous avons besoin à savoir lecture, pause, seek, chargement, stop, etc... J'ai alors rassemblé les fonctionnalités dont nous avions besoin en une classe elle même implémentée dans notre objet block reliée à nos éléments html en charge de l'affichage de ces fonctionnalités.

![](https://imgur.com/WK8xXv8.jpg)
*Exemple de blocs ainsi générés*

Derrière ses blocs se cache ainsi un objet en charge de leur génération à l'interieur duquel se trouve notre player audio.
Une des particularité de notre player contrairement à un player classique est également dans son design, la présence d'une animation de courbe sinusoïdale, comparable à une onde sonore, animée lorsque le player joue un son. J'ai été chargé de sa réalisation. Pour cela j'ai utilisé une librairie appelé SiriWave.js permettant la réalisation de courbes sinusoïdales comparables à celles utilisées dans l'animation de l'assistant vocal d'apple présent sur leurs appareils : Siri.
J'ai donc adapté notre player en créant une zone où jouer cette animation en arrière plan, puis il a fallu dessiner les différentes courbes puisque dans l'effet souhaité nous voulions un ensembles de courbes plus ou moins fines avec un déphasage permettant l'obtention d'un effet satisfaisant à regarder.

On déclare alors un espace dans lequel on veut jouer notre animation
On précise ses différents paramètres à savoir la taille de cet espace (ici la largeur de l'écran en largeur et un tiers de la hauteur de l'écran), la manière d'étirer le contenu sans le déformer pour qu'il prenne le maximum de cet espace pour s'afficher (ici c'est le paramètres "cover" qui l'indique), la vitesse d'animation c'est à dire la vitesse à laquelle les courbes s'animent, l'amplitude définissant la hauteur maximum et minimum du sommet de la courbe permettant des crêtes plus ou moins grandes, et la fréquence indiquant le nombre de crêtes de notre signal.

```javascript
var wave  =  new  SiriWaveBlock({
	container:  waveform,
	width:  document.documentElement.clientWidth,
	height:  document.documentElement.clientHeight  *  0.3,
	cover:  true,
	speed:  0.03,
	amplitude:  0.7,
	frequency:  2
});
```
Une fois nos paramètres initialisés on appelle notre classe SiriWaveBlock pour dessiner nos courbes et les animer.

```javascript
SiriWaveBlock.prototype._draw = function() {
      if (this.run === false) return;
    
      this.phase = (this.phase + Math.PI*this.speed) % (2*Math.PI);
    
      this._clear();
      this._drawLine(-2, 'rgba(' + this.color + ',0.3)', 3);
      this._drawLine(-6, 'rgba(' + this.color + ',0.5)', 3);
      this._drawLine(4, 'rgba(' + this.color + ',0.7)', 3);
      this._drawLine(2, 'rgba(' + this.color + ',0.9)', 3);
      this._drawLine(1, 'rgba(' + this.color + ',1)', 4);
    
      if (window.requestAnimationFrame) {
        requestAnimationFrame(this._draw.bind(this));
        return;
      };
      setTimeout(this._draw.bind(this), 20);
};

SiriWaveBlock.prototype._drawLine = function(attenuation, color, width){
      this.ctx.moveTo(0,0);
      this.ctx.beginPath();
      this.ctx.strokeStyle = color;
      this.ctx.lineWidth = width || 1;
    
      var i = -2;
      while ((i += 0.01) <= 2) {
        var y = this._ypos(i, attenuation);
        if (Math.abs(i) >= 1.90) y = this.height_2;
        this.ctx.lineTo(this._xpos(i), y);
      }
    
      this.ctx.stroke();
};
```
Dans cet extrait, j'ai isolé les deux fonctions principales de dessins des courbes. La fonction principale est la fonction draw() qui est appelé à chaque frame. Une frame est un laps de temps durant lequel un ensemble d'instructions est executé. Pour assure une fluidité convenable il est convenable d'avoir un minimum d'une vingtaine de frame par secondes. Dans cette fonction on dessiner ainsi nos 5 courbes à chaque frame. Ces dernières sont dessinées dans un canvas, un élément html dans lequel on peut dessiner facilement toute sorte d'objet. Il faut à chaque frame effacer ce canvas à l'aide de la fonction clear() puis y redessiner nos courbes avec le changement voulu pour former une animation.
Pour dessiner ces courbes on utilise ainsi la fonction draw_line(). Cette dernière est chargée de traduire nos paramètres en fonction mathématiques qui elles mêmes sont traduites en courbes dessinées dans notre canvas. Cette fonction mathématique est détaillée dans la boucle while, le calcul consiste à définir les cordonnées x et y du point à dessiné. Le x est une valeur qui évolue constamment, il fonctionne comme un incrémenteur et le y est la valeur qui nous intéresse, c'est elle qui créera les crêtes de notre courbe, pour obtenir précisement cette valeur on fait appel à plusieurs autre fonctions avancées non détaillées ici.
A la fin de cette fonction on dessine cette courbe à l'aide de la fonction stroke().

Au final on obtient le résultat suivant :

![](https://imgur.com/e3ty5jK.gif)
*Player Animation*

Lors du post d'un flow, l'utilisateur peut choisir de mettre une image en fond du flow. Pour ce faire il a deux possibilités, soit utiliser la caméra de l'appareil et directement prendre une photo depuis l'application, soit utiliser une photo présente sur l'appareil depuis sa gallerie. Pour ces deux fonctionnalité je fais appel à des services natifs à Android. De la même manière que lors de l'enregistrement audio, j'utilise Cordova pour faire la passerelle entre le conteneur web et les classes java permettant l'accès à l'appareil photo et à la gallerie.
Si l'utilisateur ne précise aucune photo, on génère un fond d'écran aléatoire par défaut. Pour ce faire, j'utilise une librairie appelée Geopattern proposant la génération aléatoire de forme géométrique à partir d'une chaine de caractères. J'ai adapté cette librairie pour obtenir une image de fond aux formes et couleurs variées générées à partir du timestamp au moment de l'enregistrement du flow. Ainsi, l'image alors générée est unique pour chaque flow sans jurer avec l'interface de l'application pour autant.
On peut voir un exemple de cette génération sur le gif ci-dessus qui utilise cet algorithme.

--- 
### Stories

La dernière fonctionnalité sur laquelle j'ai travaillé a été la mise en place de stories. En effet, à la manière d'un Snapchat ou d'un Instagram, nous avons jugé qu'intégrer un système de stories serait particulièrement pertinent au sein de FLOW.

Pour rappel, une story dans FLOW propose à un utilisateur de poster un ou plusieurs audio de 15 secondes maximum qui seront disponibles à tous les abonnés de cet utilisateur. Ces derniers seront accessibles uniquement durant 24h, contrairement à des flows classiques, une story ne possède pas de titre ni d'image de fond. En revanche un dégradé y est associé, sélectionné par l'utilisateur au moment du post de la story.

Pour mettre en place un tel système, j'ai d'abord conçu une interface dynamique propre à l'affichage de cette interface, sa particularité est de s'afficher à la manière d'une popup par dessus la page d'accueil de l'utilisateur. Les différentes stories sont récupérées en deux temps, dans un premier temps, on récupère depuis le serveur les personnes ayant posté une story parmi les abonnements de l'utilisateur. Ces utilisateurs s'affichent alors en haut de la page d'accueil et ceux dont l'utilisateur n'a pas encore écouté la story sont mis en valeur par une bordure aux couleur de l'application.
Dans un second temps, lorsque l'on clique sur la story en question, on effectue alors une nouvelle requête au serveur pour récupérer toutes les stories disponibles de l'utilisateur en question. Affichées une par une, il est possible de naviguer entre ces stories d'un appui à gauche ou à droite de l'écran. Il est également possible de réagir et d'accèder aux différentes réactions d'une story d'un swipe vertical vers le haut qui permet d'accéder à différentes informations telles que le nombre de vue et profils ayant consulté la story ainsi que les commentaires audio d'utilisateurs sur cette story avec la possibilité de nous aussi réagir à cette story par un enregistrement audio de 15 secondes.
D'un point de vue technique, cet onglet réutilise une version modifiée de mon player audio personnalisé. La difficulté de mise en place de cette fonctionnalité a résidé dans la récupération asynchrone des stories avec affichage d'un chargement le temps de récuperer les informations de la story et dans la récupération préalable des utilisateurs avec une story disponible de manière efficiente.

Pour jongler entre les story des utilisateurs disponibles et les différentes stories postées par tel ou tel utilisateur j'utilise deux tableaux. Un premier tableau contient tous les utilisateurs disposant d'au moins une story disponible. Chaque élément de ce tableau contient alors à son tour un tableau des stories de cet utilisateur. Mes éléments de mon premier tableau s'appellent Story tandis que ceux de mon deuxième sont des Story_flow.
```javascript
class Story {
    constructor() {
        this.user_id = 1;
        this.private_id = "Pamela";
        this.user_picture = "src/pictures/girl1.jpg";
        this.data = [];
        this.lastStoryTime = 0;
    }

    addStoryFlow(time) {
        let new_storyFlow = new StoryFlow();
        new_storyFlow.time = time;
        this.data.push(new_storyFlow);
    }
}

class StoryFlow {
    constructor() {
        this.time = "13h55";
        this.audio = new Audio("src/sound/son.opus");
        this.duration = 0;
        this.comments = [];
        for (let i = 0; i < 5; i++) {
            this.comments.push(new StoryComment());
        }
        this.seen = [];
        for (let i = 0; i < 15; i++) {
            this.seen.push(new StorySeen());
        }
    }
}

class StoryComment {
    constructor() {
        this.time = "14h56";
        this.audio = new Audio("src/sound/son.opus");
        this.user_id = 1;
        this.private_id = "Pamela";
        this.user_picture = "src/pictures/girl1.jpg";
        this.isPlaying = false;
    }
}

class StorySeen {
    constructor() {
        this.time = "Seen 5m ago";
        this.private_id = "@John";
        this.user_picture = "src/pictures/guy1.jpg";
    }
}
```
Voici ci-dessus les 4 classes principales que j'utilise pour cette fonctionnalité avec pour chaque un exemple de données type pour expliciter leur fonctionnement. Story contient toutes les informations de l'utilisateur tel que son pseudo unique appelé private_id, sa photo de profil et des données utilisées pour déterminer si l'utilisateur a déjà vu sa story ou non. Cet objet contient un tableau de StoryFlow qui eux correspondent à une story audio en particulière. Cet objet contient alors l'heure à laquelle il a été posté, le chemin vers son fichier audio, la durée de ce dernier et deux tableaux. Le premier contenant la liste des commentaires de cette story, le second la liste des gens ayant vu/écouté celle-ci.
Un commentaire d'une story aussi appelé réaction correspond à un objet StoryComment qui contient à peu de choses près les mêmes informations qu'un StoryFlow tandis qu'une personne ayant vu une story sera listé dans un objet StorySeen répertoriant l'heure à laquelle il a vu la story, son pseudo et sa photo de profil.
La concaténation de ces divers éléments permet l'obtention d'un système complet de post et de récupération de stories.

![](https://imgur.com/F2fuAP5.gif)
*Exemple de fonctionnement de l'onglet story*

Le fonctionnement de cette interface achevé, il a fallu par la suite relié le fonctionnement de ces différents services à de véritables échanges et sauvegardes de données sur le serveur. Pour cela, j'ai travaillé également sur la partie back-end de notre application et c'est son fonctionnement et les différentes réalisations opérées pour ce dernier que nous allons aborder dans la suite de ce dossier.

## Developpement Back-end

# CNIL-RGPD

# Notes RGPD

## 1. Développer en conformité avec le RGPD

Si le projet est un projet d’équipe, il est recommandé d’identifier une personne chargée du pilotage de sa conformité. Il est préférable, au sein de l’entreprise, qu’une personne doit délégué a la protection des données (DPO). Dans certains cas, ce dernier peut-être obligatoire, si le programme traitent des données nommées « Données sensibles » a grande échelle, ou si il réalise un suivi régulier et systématique à grande échelle.

Il est important de cartographier les traitement réalisés par le programme. La tenue d’un registre des activités de traitement, permet d’avoir une vision globale sur ces données, pour en identifier et hiérarchiser les risques associés. Les données personnelles peuvent parfoir se retrouver dans des endroits tels que : 

    • Les fichiers de cache
    • Les logs serveur
    • Les fichiers excel

La tenue d’un registre des activité de traitement est donc obligatoire dans la plupart des cas.


Il faut, en amont, identifier les actions à mener pour être conforme aux obligations RGPD, et prioriser les points d’attention en fonction. Ces derniers concernent nottament l’utilité et les types de données collectées et traitées par le programme. 


Il faut s’assurer que les données personnelles identifiées à risque élevés pour les personnes concernées sont bien gérées et sécurisées. Une Analyse d’Impact relative à la Protection des Données (AIPD) peut aider a maitriser ces risques. 
La CNIL fourni des méthodes à ce propos.

L’AIPD est obligatoire pour tous les traitement susceptibles d’engendrer des risques élevés pour les droits et libertés des personnes concernées. 
La CNIL propose une liste des types d’opérations de traitement pour lesquelles une AIPD est requise ou non.

Pour s’assurer d’ếtre en conformité durant les étapes du développement, il faut veiller à ce que les procédures internes prennent en compte la protection des données, ainsi que les événèment susceptibles de survenir, tels que :

    • Les failles de sécurité
    • La gestion des demandes de rectification ou d’accès
    • La modification des données collectées
    • Le changements de préstataire.

Bien que plus octroyé par la CNIL suite à l’entrée en vigueur du RGPD, les exigences du « Label gouvernance » peut constituer une base d’inspiration pour la mise en place de l’oganisation.

Afin de prouver la conformité RGPD d’un projet, toutes les actions réalisées et les documents produits doivent être maitrisés.

## 2. Identifier les données personnelles

Les données personelles sont des données relatives à une ou des personnes physiques. Par exemple : 

    • Le nom, prénom, et date de naissance d’une personne
    • Photos, enregistrements vocaux.
    • Numéro de téléphone, fixe ou portable, adresse postale, adresse mail
    • Adresse IP identifiant de connexion ou identifiant de cookie
    • Empreinte digitale, réseau veineux ou palmaire, empreinte rétinienne
    • Numéro de place d’immatriculation, numéro de sécurité sociale, numéro d’une pièce d’identité.
    • Données d’usage d’une application, commentaire, ect..

Par exemple, avec ces informations, on peut identifier une personne avec une seule information (Nom et Prénom), ou en recroisant plusieurs d’entre-elles (Une homme vivant a telle adresse, né tel jour et membre de tel communauté)

Certaines données sont considérées comme particulièrement sensibles. Le RGPD interdit tout simplement le recueil ou l’utilisation de ces données, sauf si la personne concernée a donnée son accord (Démarche active, explicite, de préférence écrite)

Les exigences ci-dessus concernent les données suivantes : 

    • Les données reliatives à la santé des individus
    • Les données concernant la vie sexuelle ou l’orientation sexuelle
    • Les données qui révèlent une pétendue origine raciale ou ethnique
    • Les opinions politiques, les convictions religieuses, philosophiques ou l’appartenant syndicale
    • Les données génétiques et biométrique utilisées aux fins d’identifier une personne de manière unique.

Le processus d’anonymisation de données personnelles a pour but de rendre impossible toute identification des individus au sein de jeux de données. Ce processus est irréversible. Si cette action est effectuée sur des données, ces dernières ne sont plus considérées comme des données personelles et les exeigences RGPD ne sont plus applicables.



Il ne faut jamais considérer des jeux de données brutes comme anynomes. Le processus d’anonymisation doit empêcher toute manière ré-identification des individus, que ce soit par : 

    • Individualisation : Il n’est pas possible d’isoler unepartie ou la totalité des enregistrement relatifs à un individu.
    • Crrélation : Le jeu de données ne permet pas de relier deux enregistrements se rapportant à une même personne ou à un groupe de personnes.
    • Inférence : Il est impossible de déduire la valeur d’un attribut d’une personne depuis des informations internes ou externes au jeu de données.

Ces traitement impliquent dans la plupart des cas une perte de qualité sur le jeu de données produit.

Information supplémentaires : 

    • L’avis G29 décrit les principales techniques d’anonymisation utilisées aujourd’hui, ainsi que des jeux de données considérés à tort comme anonymes.
    • Il n’éxiste pas de solution universelle d’anynomisation des données personelles
    • Le choix d’anonymisation et celui de sa méthode doit se faire au cas par cas selon les contextes d’usage et de besoin. (Nature, utilité, risques pour les personnes)

### La pseudonymisation des données personnelles :

Cette méthode constitue un compris entre la coservation de données brutes et la production de jeux de données anonymisées.

Elle se réfère à un traitement de données personnelles réalisé de manière à ce qu’on ne puisse plus attribuer les données relatives à une personne physique sans avoir recours à des informations supplémentaires. 

Ces informations supplémentaires doivent être stockées séparément et être soumises à des mesures techniques afin d’empêcher l’identification des personnes concernées. Contrairement a l’anonymisation, la pseudonymisation est processus reversible.

Cela consiste a remplacer les données directement identifiantes (Nom, prénom, ect) d’un jeu de données par des données indirectement identifiantes (Alias, numéro dans un classement), dans le but de réduire leur sensibilité.

Les données soumises a une pseudonymisation sont considérés comme des données personnelles et restent donc soumises aux obligations RGPD.

Le RGPD considère que la pseudonymisation permet de réduire les risques pour les personnes concernées et de contribuer la mise en conformité.


## 3. Préparer son développement.

### Choix Méthodologique

Lors de la mise en place d’un projet, il est préférable de :

    • Mettre la protection de la vie privée au coeur de vos développements en adoptant une méthodologie de Pirvacy By Design.

    • Si utilisation des méthodes agiles il y a, il faut penser a intégrer la sécurité au coeur du processus.
      
    • Si le projet est à destination du grand public, il est nécéssaire de mener une réglexion sur les paramètres relatifs a la vie privée.


### Choix technologiques :

Pour l’architecture et les fonctionnalités :

    • Il faut intégrer la protection de la vie privée, y compris les exigences de sécurité des données, dès la conception de l’application ou du service.
      
    • Garder la maitrise du système, pour garantir un haut niveau de sécurité. Un système clair, correctement conçu, et sécurisé permet une compréhension simple. En augmentant ensuite la compléxité petit à petit, il faut sécurisé les nouveautés qui s’ajoutent.
      
    • Pour minimiser les risques sur les utilisateurs finaux, il est conseillé de défendre le système en profondeur. (Exemple : Sécurité des champs d’un formulaire + A l’insertion en Base de données)


Pour les outils et les pratiques : 

    • Utiliser des normes de programmation prenant en compte la sécurité. Des outils annexes peuvent être intégrés en utilisant un IDE, pour vérifier automatiquement que le code respecte les différentes règles faisant partie de ces normes. Pour le développement WEB, des guides de bonnes pratiquement sont publiés par l’OWASP.

Le choix des technologies est crucial. Un langage peut-être plus approprié qu’un autre, en fonction du domaine d’application ou de fonctionnalité prévue.

Les langages et technologies éprouvés sont plus surs. En effet, ils font en général l’objet d’un audit afin de corriger les failles de sécurité les plus connues. Il faut cependant être vigilant et les mettres régulièrement à jour.

Il ne faut pas développer sa solution dans un langage tout juste appris. Cela accroitrai le risque de failles du fait du manque d’expérience.

## 4. Sécurité de son environnement de développement

Il faut, premièrement, recenser les mesures de sécurités existantes et définir un plan d’action permettant d’améliorer la couverture de ses risques. 

Dans un second temps, prendre en compte les risques sur les outils utilisés, notamment avec les outils SaaS et collaboratifs comme Slack, Trello, Github.

Pour faciliter le déploiement et limiter les risques, il est conseillé d'établir un document regroupent les mesures de déploiement et indiquant leur fonfiguration. Cela assurera une mise en place homogène des mesures de sécurités sur les postes et serveurs. Des outils existent tels que Ansible, Puppet ou Chef.
Il est aussi important de maintenir à jour son infrastructure, si possible automatiquement.

Pour la sécurité d'accès, il est important de mettre en place une sécurité par SSH, tout en favorisant une authentification forte sur les services utilisés par l'équipe de développement. Également, il est nécéssaire de journaliser les accès aux machines. :warning: Il est important de ne pas utiliser de compte générique.


## 5.Gérer son code source 

Un gestionnaire de code est un software permettant de stocker l'ensemble du code source et des fichiers associés, tout en conservant une chronologie de toute les modification apportées sur les fichiers.

- Il est important de bien paramétrer son environnement, via le gestionnaire de code utilisé il faut mettre en place une authentification forte (+ Authentification par clés SSH de préférence) dès le début du projet. 

- Établir des niveaux d'accès, et en définir les permissions associés. Par exemple, un "Invité" a seulement des droits restreint de lecture, et "Développeur" a les droits d'écriture.

- Faire régulièrement des sauvegardes, plus particulièrement du serveur principal.

- Surtout si plusieurs personnes développenent en même temps sur le projet, il faut mettre en place un système de branche, pour des raisons d'organisations, mais aussi de sécurité : Certains gestionnaires de codes permettent de configurer des branches protégées qui empêchent des modifications non autorisées.


Il faut aussi être vigilant sur le contenu et la qualité du code source développé.

Des outils de métriques de qualité de code permettrons de scanner le code dès son commit pour vérifier sa bonne qualité. Pour certains gestionnaires de code, il est possible suite a une configuration de refuser un commit si la qualité n'est pas satisfaisante.

:warning: Il est indispensable de conserver les mots de passes et secret en dehors du dépot. :warning:

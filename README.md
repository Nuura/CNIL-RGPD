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

   - Individualisation : Il n’est pas possible d’isoler unepartie ou la totalité des enregistrement relatifs à un individu.
   - Crrélation : Le jeu de données ne permet pas de relier deux enregistrements se rapportant à une même personne ou à un groupe de personnes.
   - Inférence : Il est impossible de déduire la valeur d’un attribut d’une personne depuis des informations internes ou externes au jeu de données.

Ces traitement impliquent dans la plupart des cas une perte de qualité sur le jeu de données produit.

Information supplémentaires : 

   - L’avis G29 décrit les principales techniques d’anonymisation utilisées aujourd’hui, ainsi que des jeux de données considérés à tort comme anonymes.
   - Il n’éxiste pas de solution universelle d’anynomisation des données personelles
   - Le choix d’anonymisation et celui de sa méthode doit se faire au cas par cas selon les contextes d’usage et de besoin. (Nature, utilité, risques pour les personnes)

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

   - Mettre la protection de la vie privée au coeur de vos développements en adoptant une méthodologie de Pirvacy By Design.

   - Si utilisation des méthodes agiles il y a, il faut penser a intégrer la sécurité au coeur du processus.
      
   - Si le projet est à destination du grand public, il est nécéssaire de mener une réglexion sur les paramètres relatifs a la vie privée.


### Choix technologiques :

Pour l’architecture et les fonctionnalités :

   - Il faut intégrer la protection de la vie privée, y compris les exigences de sécurité des données, dès la conception de l’application ou du service.
      
   - Garder la maitrise du système, pour garantir un haut niveau de sécurité. Un système clair, correctement conçu, et sécurisé permet une compréhension simple. En augmentant ensuite la compléxité petit à petit, il faut sécurisé les nouveautés qui s’ajoutent.
      
   - Pour minimiser les risques sur les utilisateurs finaux, il est conseillé de défendre le système en profondeur. (Exemple : Sécurité des champs d’un formulaire + A l’insertion en Base de données)


Pour les outils et les pratiques : 

   - Utiliser des normes de programmation prenant en compte la sécurité. Des outils annexes peuvent être intégrés en utilisant un IDE, pour vérifier automatiquement que le code respecte les différentes règles faisant partie de ces normes. Pour le développement WEB, des guides de bonnes pratiquement sont publiés par l’OWASP.

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

:warning: Il est indispensable de conserver les mots de passes et secret en dehors du dépot. :warning: Plusieurs solutions existent pour cela : 

  - Dans des fichiers à part, qui n'ont pas fait l'objet d'un commit. Il existe des solutions semi-automatique, tel que ".gitignore" pour Git. 

  - Dans des variables d'environnement, en faisant attention que ces variables ne soit pas accidentellement écrites dans les logs ou affichées dans l'application.

  - En utilisant des logiciels spécifiques de gestions de secrets ou de configuration.
  
Si par erreur des informations sensibles ont été commit, il faut purger complètement le dépot du code source, car même après modification, les données restent dans l'historique du dépot.

Il est important de toujours vérifier son code avant de le publier en ligne.
  
Si cela doit tout de même être le cas, il existe des solutions (Nommé 'Greffon'), tel que git-crypt, permettant de chiffrer/déchiffrer automatiquement les fichiers.

Des gestionnaires de code proposent ces solutitons, tel que Git, ou Mercurial, qui sont décentralisés, au contraire de SVN (Subversion), qui a besoin d'un serveur local pour fonctionner.
La plupart de ces gestionnaires proposent une interface web et des outils annexes (Wiki, gestion des bugs), ils peuvent être accessibles via Internet (Github) ou installé en interne sur vos serveurs (GitLab)


## 6.Faire un choix éclairé de son architecture

Pour avoir une vision clair du projet, il est nécésaire de décrire en amont son fonctionnement, et de schématiser le flux de données. 

Si les données sont stockées uniquement en local ou confinée sur un réseau intégralement sous la maitrîse de l'utilisateur (Wifi ou autre réseau local), le point le plus important est la sécurisation des données. Les durées de conservations sur ces données peuvent être déterminées par la personne en charge. Cependant, ces données doivent être supprimables à tout moment. 

Si, au contraire, les données doivent passer par un service en ligne, le choix d'héberger soi-même les données, ou de choisir un prestataire se fera en fonction des connaissances en sécurité, et de la qualité de service attendue. :warning: Le fait de passer par un cloud, représente un niveau de sécurité supérieur, mais genère de nouveau risque qui doivent être maitrisés.


Si recours a un prestataire d'hébergement, il est important qu'il garantisse la mise en place de mesures de sécurité et de confidentialité adaptées, et suffisamment transparentes.

Il faut aussi s'assurer de la localication géographique des serveurs qui hébergent les données. En effet, si les données peuvent circuler librement dans l'UE/EEE, il faudra assurer un niveau de protection de données suffisant et approprié en dehors de cet espace.

:warning: Si vous avec besoin d'un prestataire pour héberger des données de santé, s'assurer qu'il est certifié ou agrée pour cette activité :warning:

Les autres points a prendre en compte pour un prestataire sont :

  - L'existence d'une politique de sécurité accessible
  - Les mesure de sécurité et sûreté physique sur le site d'hébergement
  - Le chiffrement des données et autres procédé garantissant que le prestataire n'a pas accès à vous données.
  - La gestion des mises à jour
  - La réversibilité/portabilité aisée des données, dans un format couramment utilisé, sur demande à tout moment
  
## 7. Sécuriser vos sites web, vos applications et vos serveurs

### Sécuriser les communications

Pour sécuriser vos communications, voici les éléments à mettre en place : 

  - Déployer le protocole TLS 1.2 ou 1.2 (En remplacement de SSL), et rendre son utilisation obligatoire sur toutes les pages du site ou pour l'application mobiles.
  - Limitez les ports de communication strictement nécéssaires au bon fonctionnement des applications installées. Tout les autres doivent être bloqués par le pare-feu

### Sécuriser les authentifications

Il éxiste également des bonnes pratiques pour la sécurisation des authentification, à savoir : 

  - Suivre la recommandation de la CNIL sur les mots de passes (En tant qu'utilisateur d'un site). C'est a dire ne pas utiliser le même mot de passe partout, et non en rapport avec soi.
  - Ne JAMAIS stocker les mot de passes en clair. Utiliser, par exemple, Bcrypt.
  - Si des cookies sont utilisés pour l'authentification, il est recommandé de forcer l'HTTPS via l'HSTS, et d'utiliser les indicateurs "secure" et "httpOnly"
  - Désactiver les suites cryptographiques obsolotès, tel que MD4, MD5 et RC4. Favoriser l'utilisation de l'AES256.
  - Changer les mots de passes lors de chaque départ d'un administrateur en cas de suspicion de comprmission.
  - Pour les opération courantes, favoriser l'usage de compte aux privilièges moindres.
  - Pour la connexion aux serveurs internes, l'utilisation d'un VPN avec authentification forte est préconisée.
  
  
### Sécuriser les infrastructures

Afin de sécuriser les infracstructures utilisées, il est recommandé en premier lieu de faire régulièrement des sauvegardes, si possibles chiffrées et vérifiées. Cela permettra de contourner les attaques de type ransomware, par exemple.

Il est aussi important de limiter le nombre de composants mis en oeuvre (Plus il y a de composants, plus il y a de risques a gérer), et pour chacun vérifier régulièrement les mises à jours.

Pour la base de données, il est recommandé de restreindre au maximum les accès (Filtrage par IP par exemple), d'utiliser des comptes nominatifs pour l'accès, et de créer des comptes spécifique a chaque applications.
De plus, il faut, éventuellement, révoquer les privilèges d'administration des comptes, pour empêcher la modification de la structure de la base de données.
Enfin, il est indispensable de se protéger contre les injections SQL et scripts, et favoriser le chiffrement des données.

## 8. Minimiser les données collectées

Les données collectées peuvent être des données sensibles, il est important de réfléchir en amont aux différents types de données qui vont être collectées. Si des données ne sont pas nécéssaires pour tous les utilisateurs, ne pas les collecter. Également, si ce n'est pas nécéssaire, éviter de collecter des données "trop" précises (Exemple, plutot que la date de naissance, ne collecter que la date de naissance).

Comme noté ci-dessus, les données collectées peuvent être sensibles, il faut absolument veiller a collecter le STRICT MINIMUM, que ce soit directement sur son application, ou dans les fichiers de journalisation, où il ne faut pas y stocker des données de santé, des mots de passe, ect. 

Certaines fonctionnalités peuvent permettent d'améliorer l'expérience utilisateur, mais ne sont pas strictement nécéssaires au fonctionnement de l'application (La Géolocalisation par exemple). Dans ce cas, il faut laisser le choix a l'utilisateur, de choisir ou non de se faire géolocaliser. Si l'utilisateur donne une réponse positive, ces données ne doivent être concervées seulement le temps de l'utilisation de la fonctionnalité en question. Penser au temps de conservation de ces dernières.

Pour faciliter le processus, mettre en place des mécanismes d'effacement automatique, avec, par exemple : 

  - Un système de purge automatique à l'expiration de la durée de conservation des données concernées.
  - Les données représentées physiquement doivent également être détruites.
  - Si les données collectées seront utiles sur un long temps, réduire leur sensibilité avec la pseudonymisation, ou en les anonymisant.
  - Journaliser les procédures d'effacement automatique. Ces journaux peuvent être utilisés comme preuve d'éffacement d'une données.
  
## 9. Gérer les utilisateurs

### Les bonne pratiques de gestion des utilisateurs

Pour commencer, chaque invididu doit posséder des identifiants uniques, que ce soit un utilisateur de l'application, ou un collaborateur au développement. Aussi, avant d'accéder a des données personnelles, imposer une authentification.

Il faut assurer le fait que chaque utilisateur ou collaborateur ne puisse accéder strictement qu'aux données dont il a besoin. Le système doit prévoir des politiques de gestion d'accès aux données différenciées (En lecture, écriture, suppression..) suivant les utilisateurs et leurs besoins. La solution simple est un mécanisme de gestion des profils utilisateurs global, qui permettra de regrouper les différents droit en fonction d'un rôle exercé par un groupe d'utilisateurs dans l'application. Les journaux engendrés par l'utilisation de ce méchanisme ne doivent pas être conservés plus longtemps que nécéssaire. En général, une durée de 6 mois est adéquate.

### Fluidifier la gestion des profils d'habilitation

Pour garantir une sécurité, documenter ou automatiser les procédures de gestion des collaborateurs, d'inscription et de désinscription des utilisateurs. Ces procédures doivent, par exemple, encadrer la situation ou un collaborateur cesse de travail dans le projet, et ne doit plus avoir accès a des ressources.

La gestion des utilisateurs et collaborateurs impliquent une revue régulière des droits accordés, suivant la modification des usages et de l'organisation du projet. 

Enfin, il est important de ne pas utiliser le compte "super admin" pour réaliser des opérations conventionnelles. De plus, celui-ci doit être fortement protégé, et être connu par le minimum de personne possible.

## 10. Maitriser les bibliothèques et SDK

### Faire un choix éclairé

Il est nécéssaire d'évaluer l'intêret de l'ajout d'une dépendance. Plus il y a de dépendances ajoutées, plus la surface d'attaque de son système est grande. Si une bibliothèque inclût plusieurs fonctionnalités, il faut désactiver celles dont on ne se sert pas, cela réduit le nombre de bugs potentiels. (Pour Exemple, Jquery-UI, propose de lui même, de télécharger seulement les fonctionnalités dont on a besoin.) 

SCREEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEN

Plusieurs critères sont a prendre en compte lors du choix de sa bibliothèque :

  - Si l'on souhaite utiliser du code OpenSource, essayer de choisir des projets avec une communauté active, des mises à jour régulières et une documentation fournie.
  - Si l'on utilise des solutions avec un support commercial, s'assurer que le code sera maintenant le temps de la vie du projet.
  - Prendre en compte la vie privée : Certaines solutions se rénumèrent en collectant et valorisant les données personnelles. il faut s'assurer que ces solutions respectent la législation en vigueur, et qu'un mécanisme est prévu pour demander le consentement des utilisateurs.
  - Il est décosneillé d'implémenter des algorythmes ou des protocoles cryptographiques soi-même, il existe des bibliothèques en ligne reconnues, maintenues et simple d'utilisation.

### Évaluer les éléments choisis

C'est important de lire la documentation et de changer la configuration par défaut (Souvent fourni avec la dépendance). Il faut connaître le fonctionnement des dépendances incluses dans le projet. En général, le fichier de configuration par défaut présente de nombreuses failles de sécurité, il faut prendre le temps de le configurer. Aussi, c'est une bonne chose d'auditer ses bibliothèques et SDK, cela permet de déterminer les obligations à respecter au niveau de la protection des données et d'établir la résponsabilité des acteurs. Enfin, Cartographier ces dernières dans le but de mieux agir si un problème affecte l'une d'elle.

:warning: Attention au typosquattage, qui consiste a prendre un nom de dépendance très similaire a celle qui est très connue. Le paquet "typosquatté", n'est pas déployé par l'organisation de base, et peut être malveillants.


### Maintenir les bibliothèques et SDK

Pour garantir un niveau de sécurité stables, il est conseillé de :

  - Utiliser des systèmes de gestion de dépendances, qui permettent de maintenir une liste des dépendances à jour, tel que Yum, Apt, Maven ou encore Pip.
  - Gérer les mises à jour de vos dépendances le plus vite possible, surtout si elles corrigent des vulnérabilités.
  - Faire attention au versions de packages en fin de support, qui ne seront plus maintenues par la suite.
  - Surveillez les projets open sources, nottament le changement de propriétaire du domaine ou du package.
  
  
## 11. Veiller à la qualité de votre code et sa documentation 

### Documenter le code et l'architecture

Il arrive que la documentation soit mise de côté lors du développement, par manque de temps ou de visibilité. Il faut garder à l'esprit qu'elle est cruciale pour la maintenabilité du projet, que ce soit pour comprendre globalement le fonctionnement du code, ou de savoir quelles parties de ce dernier sont affectées par une modification.

Pour la documentation de l'architecture, prévilégiez des schémas et explications claires.

Il est conseillé de maintenir la documentation en même temps que le code, et également de versionner cette dernière, en assiociant chaque commit de code avec la bonne partie documentée.  

### Contrôler la qualité de votre code et de sa documentation

Un code de qualité passe par l'adoption de bonnes pratiques et de convention de codage, appliquée de manière adaptée sur l'ensemble du programme. En plus d'une convention, voici quelques bonnes pratiques : 

  - Utilisez des noms de variables et de fonctions explicites, cela favorise la compréhension globale.
  - Correctement indenter son code, cela permet de voir la structure du code plus facilement.
  - Éviter la redondance de code.
  - Pour contrôler la qualité du code, nous avons cités plus haut les plugins d'IDE, ou les logiciels de mesure de la qualité du code source, pour signaler les duplications de code, ou les bugs potentiels.
  

## 12.Tester ses applications

### Automatisations des tests

Le premier point important est l'automatisation des tests. Les tests de développement (Unitaires, fonctionnels) vont vérifier l'adéquation entre les spécifications et le fonctionnement final. Quant aux tests de sécurité, qui sont des tests a données aléatoires, vont vérifier que le code continue d'avoir un comportement acceptable si le programme est forcé de s'éloigner de son utilisation normale, et qu'il ne compte pas de faille de sécurité. Ces deux types de tests sont importants pour le bon fonctionnement de son application.

La mise en place d'un système d'intégration continue est aussi conseillée, permettant de lancer les tests automatiquement après chaque modification du code source.

### Intégrez les tests dans votre stratégie d'entreprise

Dans la mise en place de l'environnement de tests, les métriques acceptables doivent être définis conjointement par toutes les parties avant le développement.

Les métriques auxquelles il faut réfléchir sont, par exemple : 
  - Le taux de couverture des tests et leur type.
  - Le taux de réplication du code.
  - Le nombre de vulnérabilités et leur type.
  
### Attention aux données de test.

Les données "réelles" ne doivent pas être utilisées pendant la phase de développement et de test. Les utiliser revient a les détourner de leur finalité initiale. 
Si les données personnes sont tout de même utilisées hors production, il faut souligner que les risques de sécurité sont augmentés. En effet, cela provoque un accès à des données qui n'ont pas le besoin d'être connues. Cela multiplie également le    nombre d'espaces ou sont stockées ses données.

Pour éviter cela, construire un jeu de données fictives (Aussi appelé "Fixture") qui auront la structure des données qui seront traitées par l'application. La fuite de données fictives n'entrainera aucun impact pour les personnes.
Si il y a besoin d'importer et d'utiliser des configuration existantes depuis la production pour les tests, penser à anonymiser les données personnelles présentes.

## 13. Informer les personnes

### Qui informer et quand le faire ? 

Il faut informer les personnes concernées : 

  - En cas de collecte directe des données, c'est à dire lorsque des données sont recueillies directement auprès des personnes. Par exemple : Formulaire, achat en ligne, souscription d'un contrat, ouverture de compte bancaire.
  - Lors du receuil des informations via des dispositif d'observations de l'activité des personnes. Par exemple : Analyse de la navigation internet, geolocalisation, mesure d'audience.
  - En cas de collecte indirecte, c'est a dire aurpès de partenaires commerciaux, de data brokers ou de sources accessibles au public.

L'information de la collecte est nécéssaire :

  - Au moment du recueil des données, en cas de recueil directe.
  - Dès que possible en cas de collecte indirecte (Nottament lors du premier contact avec la personne) et au plus tard dans un délai d'un mois. (Sauf exeception, par exemple, oblifation légale de secret professionnel).
  - En cas d'évènement particulier ou de modification substantielle. Par exemple : Nouvelle finalité, changement dans les modalités d'exercices des droits, violation des données.
  

### Quelles informations dois-je donner ? 

Dans tout les cas, il faut préciser : 

  - L'identité et coordonnées de l'organisme qui collecte les données
  - Les finalités de cette collecte.
  - La base légale sur laquelle repose le traitement de ces données.
  - Le caractère obligatoire ou facultatif (Qui nécéssite une reflexion en amount lors du développement) et les conséquences pour la personne en cas de non-fourniture des données (Désactivation de certaines fonctionnalités par exemple)
  - Les destinataires, ou catégories de déstinataires des données.
  - La durée de conservation des données
  - L'existence des droits des personnes concernées ainsi que les moyens de les exercer (Droit d'accès, d'effacement..)
  - Les coordonnées du délégué à la protection des données de l'organisme, ou un point de contact sur les questions concernant la protection des données.
  - Le droit d'introduire une réclamation auprès de la CNIL.
  
Dans certains cas, des informations supplémentaires sont demandées, par exemple dans le cas d'un transfert de données hors de l'UE.

Si il y a une collecte indirecte, il faut ajouter : 
  - Les catégories de données recueillies.
  - La provenance des données (En indiquant si elles sont issues de sources publiques)
  
### Sous quelle forme dois-je fournir ces informations ? 

L'information doit être facile d'accès, l'utilisateur doit pouvoir la trouver dans difficultés. Elle doit être fournie de manière claire et compréhensible (Vocabulaire simple) et adaptée au public visé (Attention particulière aux enfants et personne vulnérables). Les informations doivent être écritent de manière consice, sans noyer l'utilisateur dans pleins d'informations. Il faut également pouvoir distinguer les informations qui sont liées a laa vie privée, et celles qui ne le sont pas. (Comme les clauses contractuelles)

### Quelle communication effectuer lorsque la sécurité est compromise ? 

Si un organisme, par erreur ou négligence, subit, accidentellement ou de manière malintentionnée, une violation des données (Atteinte a la sécurité des données), c'est a dire : 
  - Destruction
  - Perte
  - Altération
  - Divulgation non autorisée
doit dans les 72heures signalé la violation auprès de la CNIL (Si les données présentent un risque pour les droits et libertés des personnes).

Si le risque est trop élevé, l'organisme a pour obligation d'informer les personnes concernées le plus rapidement possible, et d'adresser des conseils à ces dernières (Annulation carte bancaire, modification mot de passe, ect)

Enfin, la notification de la violation à la CNIL doit se faire via le site web de la CNIL.


## 14. Préparer l'exercice des droits des personnes

### Les mesures minimales à mettre en place

Tous les organismes utilisant des données personnelles ont l'obligation d'indiquer où et comment les personnes peuvent exercer leur droits relatifs à ces données. Par exemple, dans la politique de vie privée du projet.

Voici quelques exemples de droits et leur possible implémentation :

Le droit d'accès : Les personnes ont le droit de demander et d'obtenir une copie de toutes les informations que vous avez à leur sujet. Cela permet au demandeur de savoir si des données lui appartenant sont traitées et d'en obtenir une copie. Également, cela permet de contrôler l'exactitude des données.
- Implémentation : Prévoir une fonctionnalité affichant toutes les données relatives à une personne. Si les données sont trop volumineuses, proposer le téléchargement d'une archive.

Le droit a l'effacement : Les personnes ont le droit de demander l'effacement de l'intégralité des données que l'on détient sur elles.  
- Implémentation : 
    - 1. Prévoir une fonctionnalité permettant d'effacer toutes les données relatives à une personnes.
    - 2. Prévoir une notification automatique qui prévient les sous-traitants afin qu'ils effacent également les données.
    - 3. Prévoir un effacement dans les sauvegardes, ou tout autre support permettant la restauration de ces données.

Le droit d'opposition : Dans certains cas, les personnes ont le droit de s'opposer à ce que leur données soient utilisées pour un objectif précis.
- Implémentation : Prévoir une fonctionnalité permettant à la personne de s'opposer au traitement. Si la personne exerce son droit, le responsable doit supprimer les données la concernant, et ne plus en collecter.
 
Le droit de portabilité : 
Les personnes ont le droit de récuperer leur données dans un format lisible par machine, pour leur propore usage ou pour les fournir à un autre organisme.
- Implémentation : Prévoir une fonctionnalité d'export au format lisible par un ordinateur(CSV, XML, JSON, ect)

Le droit de rectification : Les personnes ont le droit de demander la modification de leurs données lorsque celles-ci sont incorrectes afin de limiter l'utilisation ou la diffusion d'informations érronées.
- Implémentation : Permettre a l'utilisateur de pouvoir modifier ses données.

Le droit à la limitation du traitement : Les personnes ont le droit de demander à ce que le traitement de leurs données soit bloqué pendant un certain temps, par exemple le temps d'examiner une contestation de sa part sur l'utilisation de ses données ou une demande d'exercice de droits.
- Implémentation : Permettre aux administrateurs de mettre des données relatives à une personne en "quarantaine" : Ces données ne pourront alors plus être lues ou modifiées.

## 15. Gérer la durée de conservation des données

### Les cycles de conservation des données.

Le cycle de conservation des données personnelles peut être divisé en 3 phases succéssives distinces :

- La base active 
- L'archivage intermédiaire
- L'archivage définitif ou la suppression

Ces méchanismes de suppresions de données des bases actives permettent de garantir que les données sont conservées et accessibles par les services opérationnels uniquement le temps nécéssaire à l'accomplissement de l'objectif poursuivi par le traitement.
Il ne faut pas conserver les données en base actives en les notant simplement comme archivées. les données archivées (Les archives intermédiaire donc) ne doivent être accéssible qu'a un service spécial chargé d'y accéder et de les sortir des archives le cas échéant.
Il faut donc veuiller a prévoir des modalités d'accès spécifique à ses archives, car l'utilisation d'une archive doit rester ponctuelle et exceptionnelle.
Si possible, mettre en place la même implémentation lors de la mise en oeuvre de la purge ou de l'anonymisation des données que celle gérant le droit a l'effacement. Celui permet de garantir un fonctionnement homogène du système.

### Exemple de durée de conservation

  - Les données relatives à la gestion de la paie ou au contrôle des horaires des salariés peuvent conservées pendant 5ans maximum.
  - Les données figurant dans un dossier médical doivent être conservées 20 ans.
  - Les coordonnées d'un prospect ne répondant à aucune sollicitation peuvent être conservées pendant 3 ans.
  - Les données de journalisation peuvent être conservées durant 6 mois.
  
## 16. Gérer la durée de conservation des données

### Définition des bases légales prévues par le RGPD

Pour les développements pour un organisme privé (Entreprises, associations, ect), les bases légales les plus utilisées sont : 

  - Le contrat : Le traitement est nécessaire à l'exécution ou à la préparation d'un contrat entre la personne concernée et l'organisme mettant en place le traitement.
  - L'intêret légitime : L'organisme mettant en place le traitement poursuit un intérêt "légitime" à mettre en place le traitement et celui-ci n'est pas suspectible d'affecter les droits et libertés des personnes concernées.
  - Le consentement : La personne concernée a explicitement consenti au traitement.
  
 Si, le développement est pour un organisme poursuivant des missions d'intérêt public, d'autres bases légales peuvent être utilisées : 
  - L'obligation légale : Le traitement doit-être imposé par des textes réglementaires.
  - La mission d'intêret public : Le traitement est nécessaire à l'exécution d'une mission d'intérêt public.
  
Des fiches pratiques sont mises à disposition par la CNIL afin d'accompagner dans le choix des bases légales les plus adaptes à vos traitements. La CNIL propose également de vérifier depuis leur site, qu'un texte n'impose pas de contraintes particulères (Prospection commerciale par voie éléctronique, traceurs, ect).

Enfin, dans des cas très spécifiques, la sauvegarde des intêrets vitaux peut être retenue comme base légale. (Pour éviter la propagation d'épidémies, ou des cas d'urgence humanitaire par exemple.)

### Choisir la base légale adéquate

Dans ce choix, une seule base doit-être choisie pour une finalité donnée. Il n'est pas possible de cumuler pour une même finalité. Si l'organisme est public, l'obligation légale et la mission d'intérêt public seront les plus pertinentes dans la majorité des cas.

Si le traitement s'inscrit dans une relation contractuelle et que sa finalité est objectivement et strictement nécessaire à la fourniture du service de l'utilisateur (Par exemple, dans le cadre d'un site E-commerce, le nom, prénom et adresse pour créer un  compte), alors la base légale du contrat devrait être appropriée.

Si, au contraire, le traitement ne s'inscrit pas dans une relation contractuelle avec l'utilisateur, les bases légales du consentement ou de l'intérêt légitime peuvent être mobilisées. Si le traitement est intrusif (Profilage, collecte géolocalisation), le consentement est susceptible d'être la base légale appropriée.

Si le traitement contient des données sensibles, il faudra, en plus de la base légale, identifier une exception prévue par l'article 9 du RGPD (La personne donne son consentement explicite, par exemple)


### Les exercices de droits et les modalitées d'information à prévoir suivant la base légale

Ci-dessous un tableau récapitulant les exercices des droits à prevoir suivant les bases legales choisies : 

SCREEEEEEEEEEEEEEEN

Les bases légales doivent toujours figurer dans les informations transmises à la personne. De plus, lorsque le traitement est fondé sur l'intérêt légitime, il faut indique les intérêts légitimes poursuivis (Lutte contre la fraude, sécurité du système)

Il est recommandé de documenter le choix des bases légales, cela aidera a cartographier les traitements associés à la documentation technique, et d'avoir une vision globale plus claire.

### Le cas spécifique des cookies et autres traceurs

La directive européenne ePrivacy requiert le consentement de l'utilisateur avant toute action visant à stocker des informations, que ce soit via des cookies, identifiants, des traceurs. Cette directive s'applique également avant d'accéder a des données stockées dans l'équipement de l'utilisateur.

Il éxiste cependant une exception lorsque les cookies ont pour finalité exclusive de permettre ou faciliter la communication par voie électronique, ou sont strictement nécéssaires à la fourniture du service demandé par l'utilisateur.

Remarque : Le fait d'utiliser un seul traceur pour de multiples pour de multiples finalités ne décharge pas de receuillir le consentements pour les finalités qui le nécéssitent. Par exemple, un cookie d'authentification aussi utilisé à des fins publicitaire, nécéssitera l'accord de l'utilisateur pour cette dernière finalité.


## 16. Mesurer la fréquentation de vos sites web et de vos applications

### Obtenir le consentement

En général, avant de déposer ou lire un cookie ou un traceur, les éditeurs de sites ou d'applications doivent informer les internautes de la finalités des cookies, obtenir leur consentement, et surtout leur fournir un moyen de les refuser. Il faut prendre en compte que ces contraintes sont aussi valables pour la mesure d'audience.

### Bénéficier de l'exemption de consentement

Il éxiste des exceptions concernant les cookies et traceurs utilisés pour la mesure d'audience. En effet, ils peuvent être dispensés de consentement.

Ces exceptions sont soumises a des conditions, qui sont les suivantes : 

  - D'informer les utilisateurs de leur utilisation
  - De leur donner la possibilité de s'y opposer
  - De limiter le dispositif aux seules finalités suivantes :
    - La mesure d'audience
    - L'A/B Testing (Technique de marketing consistant à proposer plusieurs variantes d'un même objet qui diffèrent selon un seul critère, la couleur par exemple)
    
  - De ne pas recouper les données traitées avec d'autres traitements (Fichier clients, statistiques de fréquentation).
  - De limiter la portée du traceur à un seul éditeur de site ou d'application.
  - De tronquer le dernier octet de l'adresse IP.
  - De limiter la durée de vie des traceux à 13 Mois.
  
Si ces conditions sont réspectées, on passe d'un régime d'opt-in à un régime d'opt-out (Opt-in : Obtenir l'accord du destinaire de la publicité (Si il n'a pas dit oui, c'est non) / Opt-out : Le destinataire de la publicité ne s'est pas opposé (S'il n'a pas dit non, c'est oui))

À noter qu'il est possible pour un même sous-traitant de fournir un service de mesure d'audience comparatif à de multiples éditeurs, sous réserve que les données soient collectées, traitées et stockées de manière indépendante pour chaque éditeur et que les traceurs soient indépendants les uns des autres.

### En pratique

En pratique, la plus grandes parties des offres de mesures d'audience ne seront pas éligibles à cette exemption, quelle que soit leur configuration
Pour bénéficier de cette exemption, il est conseillé de se rapprocher de son éditeur de logiciels, ou d'utiliser des logiciels libres tel que Piwik, qui propose de configurer ses paramètres soi-même.

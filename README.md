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

# La pseudonymisation des données personnelles :

Cette méthode constitue un compris entre la coservation de données brutes et la production de jeux de données anonymisées.

Elle se réfère à un traitement de données personnelles réalisé de manière à ce qu’on ne puisse plus attribuer les données relatives à une personne physique sans avoir recours à des informations supplémentaires. 

Ces informations supplémentaires doivent être stockées séparément et être soumises à des mesures techniques afin d’empêcher l’identification des personnes concernées. Contrairement a l’anonymisation, la pseudonymisation est processus reversible.

Cela consiste a remplacer les données directement identifiantes (Nom, prénom, ect) d’un jeu de données par des données indirectement identifiantes (Alias, numéro dans un classement), dans le but de réduire leur sensibilité.

Les données soumises a une pseudonymisation sont considérés comme des données personnelles et restent donc soumises aux obligations RGPD.

Le RGPD considère que la pseudonymisation permet de réduire les risques pour les personnes concernées et de contribuer la mise en conformité.

# Silent-cryptominer
![SilentCryptoMiner](https://github.com/azertyuiopexe/Silent-cryptominer/assets/153385259/efa6d21b-cd08-4e3a-8f3e-64213f5b8599)


SilentCryptoMiner v3.4.0 - Mineur pour ETC, RVN, XMR, RTM et bien d’autres
Un mineur de crypto-monnaie natif silencieux (caché) gratuit capable de miner ETC, RVN, XMR, RTM et bien plus encore, avec de nombreuses fonctionnalités adaptées au minage en silence.

Ce mineur peut miner tous les algorithmes suivants et donc toute crypto-monnaie qui utilise l’un d’entre eux :

Liste des algorithmes
Caractéristiques principales
C++ natif - Installateur/injecteur de mineur et chien de garde entièrement codés en C++ sans exigences d’exécution, à l’exception d’un système d’exploitation 64 bits
Injection (silencieuse / cachée) - Cacher le mineur dans un autre processus comme conhost.exe, explorer.exe, svchost.exe et autres
Inactif : peut être configuré pour miner à différentes utilisations du CPU et du GPU, ou pas du tout, lorsque l’ordinateur est ou n’est pas utilisé.
Furtivité - Met le mineur en pause et efface la mémoire du GPU et la RAM lorsque l’un des programmes de l’option « Cibles furtives » est ouvert
Chien de garde - Surveille le fichier du mineur, les processus du mineur et l’entrée de démarrage et restaure le mineur si quelque chose est supprimé ou tué
Plusieurs mineurs - Peut créer plusieurs mineurs à exécuter en même temps, par exemple un mineur XMR (CPU) et un mineur RVN (GPU)
Exploitation minière CPU et GPU - Peut miner à la fois sur CPU et GPU (Nvidia et AMD)
Exclusions de Windows Defender : peut ajouter des exclusions dans Windows Defender après avoir été démarré pour éviter d’être détecté
Process Killer - Vérifie constamment la présence de tous les programmes dans la liste « Kill Targets » et les tue s’ils sont trouvés.
Configuration à distance - Peut obtenir les paramètres du mineur à distance à partir d’une URL spécifiée toutes les 100 minutes
Prise en charge du panneau Web - Prend en charge la surveillance et la configuration efficaces de tous les mineurs dans un panneau Web en ligne auto-hébergé gratuit
Et bien d’autres encore.
Téléchargements
Précompilé : https://github.com/UnamSanctam/SilentCryptoMiner/releases

Exemples de paramètres : Exemples de paramètres

Wiki
Vous pouvez trouver le wiki ici ou en haut de la page. Le wiki contient des informations sur le mineur et toutes ses fonctionnalités, il contient également des réponses aux questions fréquemment posées.

Panneau Web
Vous pouvez trouver le panneau Web que le mineur prend officiellement en charge ici : UnamWebPanel. Le panneau Web peut être utilisé pour surveiller le taux de hachage, l’état, les paramètres de connexion de vos mineurs et plus encore. Il peut également être utilisé pour modifier les paramètres du mineur, tout comme le fait l’option « Configuration à distance ».

Journal des modifications
3.4.0 (14-11-2023)
Modification de la procédure d’installation « Démarrage » de l’administrateur de l’utilisation du planificateur de tâches à la place de l’installation en tant que service
Modification de l’installation de l’administrateur « Démarrage » de l’installation dans « Program Files » à la place de l’installation dans « ProgramData »
Suppression de l’option « Exécuter en tant que système » en raison du fait que les services s’exécutent toujours en tant que système
Ajout de la suppression de MSRT à la fonctionnalité « Ajouter des exclusions Defender »
Modification du compilateur C++ pour un compilateur avec moins de détections et de meilleures fonctionnalités
Amélioration de la procédure de démarrage du compilateur externe pour contourner les bogues du compilateur lorsque le chemin de compilation contient des espaces ou des caractères Unicode
Modification du processus de compilation afin d’y incorporer la « bande » pour supprimer tous les symboles et données de déplacement inutiles.
Ajustement du niveau d’optimisation du compilateur pour atténuer certaines détections d’antivirus
Activation de LTO pendant la compilation pour supprimer un grand nombre de détections causées par le compilateur dans les sections inutilisées
Modification de l’utilisation de fichiers temporaires par le compilateur afin de mieux fonctionner avec certains environnements irréguliers.
Modification de la procédure de compilation pour ajouter une date de création aléatoire et une date de dernière écriture aux fichiers de minage compilés
Restauration de la version de .NET Framework du générateur de mineurs vers .NET 4.5 à partir de .NET 4.8 pour une meilleure compatibilité
Modification de la technique d’injection des mineurs pour réduire la complexité et les détections antivirus
Optimisation du code de création du processus
Refonte du code de boucle d’injection de mineur et du code de boucle de vérification du mutex de chien de garde pour contourner une nouvelle détection ciblée de Windows Defender
Amélioration considérable du générateur d’appels système SysWhispersU
Passage d’appels système statiques à des appels système dynamiques aléatoires
Modification de la fonctionnalité « Exécuter en tant qu’administrateur » pour élever par programmation plutôt que par le biais d’un fichier manifeste afin d’éviter les détections causées par le manifeste
Ajout de l’obscurcissement à toutes les constantes et littéraux
Ajout de l’encodage base64 aux fichiers embarqués afin de contourner les détections causées par des données à haute entropie
Modification du format de ressource incorporé de hexadécimal à décimal afin de réduire l’utilisation de la mémoire et le temps de compilation
Modification des onglets par défaut « Démarrage » « Nom de l’entrée » et « Nom du fichier » en une chaîne aléatoire en raison du ciblage par Windows Defender des noms par défaut actuels
Ajout d’un nouveau bouton « Randomiser » à côté des onglets « Démarrage », des options « Nom de l’entrée » et « Nom du fichier » pour permettre une randomisation rapide
Ajout d’une nouvelle « option avancée » qui permet l’empaquetage UPX automatique des fichiers de ressources de minage intégrés
Modification des fonctions « Désactiver Windows Update » et « Désactiver la mise en veille » pour appeler directement les programmes au lieu de les appeler via une ligne de commande
Modification du programme par défaut « Inject Into » en conhost.exe au lieu de explorer.exe en raison du fait que explorer.exe déclenche désormais des détections lors de l’exécution sous Système
Ajout de l’exclusion d’extension « .exe » à la fonctionnalité « Ajouter des exclusions Defender » afin d’empêcher potentiellement certaines détections de mémoire générales futures
Suppression de l’option XMR « GPU Mining » en raison de problèmes avec CUDA et du fait qu’elle soit pire que le mineur GPU dédié déjà existant
Suppression de l’option XMR « CPU Mining » car elle n’a plus de raison d’exister maintenant que l’option « GPU Mining » a disparu
Réécriture de la fonction de chiffrement XOR pour contourner la détection d’obscurcissement XOR
Refonte du code de la fonctionnalité « Bloquer les sites Web » pour contourner certaines détections causées par le bouclage
Amélioration considérable du code global afin de réduire le gaspillage d’appels, de poignées et d’éventuelles signatures de code
Modification du « Délai de démarrage » pour qu’il ne s’applique qu’avant l’installation afin d’éviter les délais d’attente
Mise à jour du programme de désinstallation pour supprimer correctement tous les fichiers
Mise à jour des mineurs
3.3.1 (04/09/2023)
Ajout du chargeur OpenCL ICD de manière statique dans le mineur GPU, car les chargeurs locaux de certains systèmes ne semblent pas fonctionner
Ajout d’un redémarrage automatique du cœur de minage du processeur lorsqu’une période prolongée de taux de hachage nul est détectée
Correction du déclencheur « Démarrage » de l’administrateur pour qu’il soit « à la connexion » lorsque « Exécuter en tant que système » est désactivé
Réduction de certaines détections antivirus en modifiant la commande de compilation miner
Modification de certaines commandes du compilateur de miner builder pour qu’elles soient absolues au lieu de relatives
Ajout de l’onglet « Assemblage » Nettoyage du numéro « Version »
Correction d’un avertissement de journal inutile lors de la compilation
Suppression de nombreuses anciennes chaînes de débogage inutilisées à l’intérieur des mineurs
3.3.0 (24/08/2023)
Ajout de l’algorithme KawPow (kawpow) directement dans le mineur GPU
Ajout d’un nouvel algorithme FiroPow (firopow)
Ajout d’un nouvel algorithme ProgPow (progpow)
Ajout d’un nouvel algorithme ProgPowZ (progpowz)
Ajout d’un nouvel algorithme EvrProgPow (evrprogpow)
Mise en œuvre de KawPow, FiroPow, EvrProgPow, ProgPow et ProgPowZ en utilisant uniquement OpenCL pour Nvidia et AMD afin de contourner les exigences de la grande bibliothèque CUDA NVRTC.
Réécriture de la majeure partie du mineur GPU pour ajouter la prise en charge de plusieurs familles d’algorithmes et améliorer considérablement la stabilité et la fiabilité
Ajout du protocole Sero-Proxy pour pouvoir miner Sero (ProgPow)
Suppression de l’algorithme KawPow (kawpow) du mineur XMR et de la grande bibliothèque CUDA NVRTC pour s’assurer que personne ne l’utilise accidentellement
Ré-ajout de l’algorithme Panthera (rx/xla)
Ajout de la prise en charge de l’exploitation minière en solo de la pièce Zéphyr (rx/0)
Déplacement de l’option « GPU Mining » du mineur XMR dans l’onglet « Avancé » pour décourager le minage de GPU XMR non rentable
Déplacement de l’option « Utiliser le rootkit » dans les « Options avancées » pour plus de clarté quant à sa complexité.
Modification de la création de tâches du planificateur de tâches de Powershell à l’utilisation uniquement de la ligne de commande avec un fichier XML temporaire
Modification du chemin d’accès du pilote MSR de l’utilisation d’un chemin d’accès de bibliothèque statique à un chemin généré dynamiquement
Modification du chiffrement et du déchiffrement des fichiers intégrés pour réduire les détections heuristiques
Modification de la version du compilateur de code pour une version différente afin de réduire considérablement les détections antivirus causées par le compilateur
Amélioration des commandes d’exécution du compilateur externe en forçant mieux les chemins absolus dans les commandes
Ajout d’un mutex dans l’installateur/injecteur du mineur pour le rendre vérifiable par le chien de garde
Réduction de l’intervalle de vérification du chien de garde pour une meilleure persistance
Suppression des fonctions d’assistance inutilisées
Réécriture de la fonction de tueur de mineurs des désinstallateurs pour qu’elle fonctionne avec les ID de processus au-dessus de la limite ushort
Modification de l’initialisation de la chaîne Unicode d’une macro à une fonction pour réduire la taille finale du code
Modification de la mise en forme des chaînes de l’utilisation de l’API Windows intégrée à l’utilisation d’une fonction personnalisée beaucoup plus petite
Déplacement des rapports du panneau Web avant le changement d’utilisation de l’inactivité du processeur afin de rendre le taux de hachage moins déroutant.
Amélioration de la vitesse de régénération de la base de données RandomX lorsque vous quittez « Furtivité » sur des pools avec de nouvelles tâches peu fréquentes.
Correction de la valeur de configuration par défaut « Furtivité en plein écran » lorsque « Exécuter en tant que système » était désactivé
Correction d’un éventuel problème de comptage de la longueur de la chaîne de terminaison nulle dans la fonction de vérification du GPU
Réduction de la taille de la pile de fonctions de création de répertoires récursives inutiles
Modification de l’état d’exécution des mineurs pour qu’il ne soit plus toujours en mode veille semi-bloc sur certains ordinateurs
Restructuration de la liste de sélection de l’algorithme pour qu’elle soit plus facile à utiliser
Ajout d’une fonctionnalité semi-CLI pour la construction de mineurs via la ligne de commande
Mise à jour du rootkit vers une nouvelle version
Vous pouvez consulter le changelog complet ici

Auteur
Unam Sanctam
Contributeurs
Werlrlivx - Traduction polonaise
Xeneht - Traduction Espagnole
BITIW - Traduction en russe
MatheusOliveira-dev - Portugais (Brésil) Traduction
Démenti
En tant que créateur, je ne suis pas responsable des actions et/ou des dommages causés par ce logiciel.

Vous assumez l’entière responsabilité de vos actes et reconnaissez que ce logiciel a été créé à des fins éducatives uniquement.

L’objectif principal de ce logiciel est de NE PAS être utilisé à des fins malveillantes, ou sur un système que vous ne possédez pas ou que vous n’avez pas le droit d’utiliser.

En utilisant ce logiciel, vous acceptez automatiquement ce qui précède.

Licence
Ce projet est sous licence MIT - voir le fichier LICENSE pour plus de détails

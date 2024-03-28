Installation de Docker

    Mettez à jour votre liste de paquets :

$sudo apt update

Installez les dépendances nécessaires pour ajouter les packages via HTTPS :

$sudo apt install apt-transport-https ca-certificates curl software-properties-common

Ajoutez la clé GPG officielle de Docker :

$curl -fsSL https://download.docker.com/linux/debian/gpg | sudo apt-key add -

Ajoutez le référentiel Docker à vos sources de logiciels APT :

$sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/debian $(lsb_release -cs) stable"

Mettez à jour à nouveau la liste des paquets :

$sudo apt update

Installez Docker Community Edition :


$sudo apt install docker-ce

Vérifiez que Docker s'est bien installé en exécutant la commande :

$sudo docker --version

Ajoutez votre utilisateur au groupe Docker pour pouvoir exécuter des commandes Docker sans sudo (remplacez utilisateur par votre nom d'utilisateur) :

$sudo usermod -aG docker utilisateur

Démarrez le service Docker :

$sudo systemctl start docker

Pour que Docker démarre automatiquement au démarrage du système, activez le service :

    $sudo systemctl enable docker

Installation de Docker Compose

    Téléchargez la version stable de Docker Compose (vérifiez la dernière version sur https://github.com/docker/compose/releases) :


$sudo curl -L "https://github.com/docker/compose/releases/download/{version}/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose

Assurez-vous de remplacer {version} par la version de Docker Compose que vous souhaitez installer.

Rendez le binaire téléchargé exécutable :

$sudo chmod +x /usr/local/bin/docker-compose

Vérifiez que Docker Compose s'est bien installé en exécutant la commande :


    $docker-compose --version

Après avoir suivi ces étapes, Docker et Docker Compose devraient être installés et prêts à être utilisés sur votre machine Parrot OS. N'oubliez pas de vous déconnecter et de vous reconnecter (ou de redémarrer votre système) après avoir ajouté votre utilisateur au groupe Docker pour que les modifications prennent effet.

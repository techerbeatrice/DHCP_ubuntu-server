## DHCP server sur ubuntu : installation, configuration et test   

***
- Dans un terminal, saisir la commande suivante pour installer le serveur DHCP :

#### $ sudo apt install isc-dhcp-server

![image](https://github.com/techerbeatrice/DHCP_ubuntu-server/assets/138071140/2a246765-c852-4752-a8e4-b81b976b86f2)

***
- Modifier le fichier de configuration selon vos besoins en spécifiant les paramètres DHCP, pour cela éditer dans le fichier de configuration DHCP avec la commande :
   
#### $ sudo nano /etc/dhcp/dhcpd.conf

![image](https://github.com/techerbeatrice/DHCP_ubuntu-server/assets/138071140/ffd2ffbf-c3bb-478c-9c71-ea19bcf4ebb9)

***

- Faire un **ip a** pour obtenir des informations sur les interfaces réseau de la machine :

![image](https://github.com/techerbeatrice/DHCP_ubuntu-server/assets/138071140/8cf15c8c-71cc-4fa9-981c-2106f97d0c39)

***

- Définir l'interface réseau que DHCP server doit utiliser pour répondre aux requêtes DHCP des clients en renseignant le nom de l'interface réseau ; dans notre exemple cette interface s'appelle **enp0s3** :

![image](https://github.com/techerbeatrice/DHCP_ubuntu-server/assets/138071140/7f5e2899-0186-4537-a577-143948b86fd7)

***

- 

✔ Donner le rôle DHCP à windows Server, pour cela aller dans Gérer --> Ajouter des rôles et fonctionnalités --> Dans Type d'installation, sélectionner Installation basée sur un rôle ou une fonctionnalité --> Dans sélection du serveur --> Sélectionner un serveur du pool de serveurs --> Sélectionnner le serveur de destination --> Dans la liste des rôles, cochez Serveur DHCP

![image](https://github.com/techerbeatrice/DHCP_windows-server/assets/138071140/ec8351da-245a-4833-8db1-194e5bd42969)

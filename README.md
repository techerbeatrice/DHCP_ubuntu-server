## DHCP server sur ubuntu : installation, configuration et test   

***
✔ Dans un terminal, saisir la commande suivante pour installer le serveur DHCP :

#### $ sudo apt install isc-dhcp-server

![image](https://github.com/techerbeatrice/DHCP_ubuntu-server/assets/138071140/2a246765-c852-4752-a8e4-b81b976b86f2)

***
✔ Configurer la carte réseau en Réseau Interne :

![image](https://github.com/techerbeatrice/DHCP_ubuntu-server/assets/138071140/2883a7e2-7061-4ef0-8735-a0b9d98ce3a9)

***

✔ Attribuer une adresse IP au serveur DHCP :

![image](https://github.com/techerbeatrice/DHCP_ubuntu-server/assets/138071140/133bb725-e638-4a3e-98af-83f686c2bcbd)

***

✔ Modifier le fichier de configuration selon vos besoins en spécifiant les paramètres DHCP, pour cela éditer dans le fichier de configuration DHCP avec la commande :
   
#### $ sudo nano /etc/dhcp/dhcpd.conf

![image](https://github.com/techerbeatrice/DHCP_ubuntu-server/assets/138071140/ffd2ffbf-c3bb-478c-9c71-ea19bcf4ebb9)

***

✔ Faire un **ip a** pour obtenir des informations sur les interfaces réseau de la machine :

![image](https://github.com/techerbeatrice/DHCP_ubuntu-server/assets/138071140/8cf15c8c-71cc-4fa9-981c-2106f97d0c39)

***

✔ Définir l'interface réseau que DHCP server doit utiliser pour répondre aux requêtes DHCP des clients en renseignant le nom de l'interface réseau ; dans notre exemple cette interface s'appelle **enp0s3** :

![image](https://github.com/techerbeatrice/DHCP_ubuntu-server/assets/138071140/7f5e2899-0186-4537-a577-143948b86fd7)

***

✔ Démarrer le serveur DHCP avec la commande suivante :

#### $ service isc-dhcp-server start et $ service isc-dhcp-server status

![image](https://github.com/techerbeatrice/DHCP_ubuntu-server/assets/138071140/6d8ef047-697e-45df-9027-bbff194f8c7b)

***

✔ Démarrer une machine cliente configurée en Réseau Interne :

![image](https://github.com/techerbeatrice/DHCP_ubuntu-server/assets/138071140/4ac5f870-1d16-4b40-b4ed-dcb5ae0d2d2a)

- Le serveur DHCP lui a bien fourni une adresse IP réservée passant par les étapes du processus DORA  (DHCP DISCOVER, DHCP OFFER, DHCP REQUEST, DHCP ACK) :
  
![image](https://github.com/techerbeatrice/DHCP_ubuntu-server/assets/138071140/1e90e237-942e-4bdd-9d50-8c6383c1b7cc)

![image](https://github.com/techerbeatrice/DHCP_ubuntu-server/assets/138071140/91e87ded-4df2-4996-b3d0-a8079fca58ff)

- Après une **ipconfig /release** et une **ipconfig /renew**, la machine cliente obtient la même adresse IP.

![image](https://github.com/techerbeatrice/DHCP_ubuntu-server/assets/138071140/6053f2c1-e20d-43e2-80e9-a68c0f0af5bd)

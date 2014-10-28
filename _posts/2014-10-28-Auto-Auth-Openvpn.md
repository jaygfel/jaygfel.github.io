---
layout : post
title : How to auto-auth Openvpn
---

Pour pouvoir lancer Openvpn en fond depuis une sessions SSH avec `sudo nohup openvpn /path/to/openvpn.ovpn &` il faut activer l'auto-auth de la configuration Openvpn.
Pour cela il faut :

1. Créer un fichier mdp.pass (au tout autre nom) comprenant les données de connexion 
`username`
`password`

2. Ajouter ou modifier la ligne correspondant à l'auth dans le fichier de config openvpn (`/path/to/openvpn.ovpn`) pour obtenir la ligne suivante :
`auth-user-pass mdp.pass`


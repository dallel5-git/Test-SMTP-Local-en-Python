# Python Local SMTP Server Demo

Une démonstration simple et efficace de configuration d'un serveur SMTP local en Python pour intercepter et tester l'envoi d'e-mails en environnement de développement local.

---

## Démonstration en Action

<img width="640" height="360" alt="Vidéo sans titre" src="https://github.com/user-attachments/assets/e1e44fb3-1ae1-43b1-91d1-8347825560eb" />


---

## Objectif du Projet

Lors du développement d'applications web ou de scripts envoyant des e-mails, il est souvent risqué d'utiliser un vrai serveur SMTP en phase de test. Ce projet montre comment utiliser le module Python `aiosmtpd` pour créer un serveur SMTP fictif qui reçoit et affiche les e-mails directement dans la console sans les envoyer réellement.

---

## Prérequis

- **Python 3.7+**
- Le package `aiosmtpd`

Installez la dépendance requise via pip :

```bash
pip install aiosmtpd
```

🚀 Utilisation
1. Lancer le serveur SMTP local
Ouvrez un premier terminal et exécutez le serveur SMTP simulé sur le port 1025 :

Bash
python -m aiosmtpd -n -l localhost:1025
2. Tester l'envoi d'e-mails
Dans un second terminal, vous pouvez tester la réception en vous connectant via telnet ou un client SMTP :

```Bash
telnet localhost 1025
```
Puis envoyez une commande SMTP de test :

Extrait de code
HELO localhost
MAIL FROM: <sender@example.com>
RCPT TO: <recipient@example.com>
DATA
Subject: Demo presentation

Ceci est un test pour montrer le fonctionnement du protocole SMTP.
.
QUIT


👤 Auteur
Oussama Dallel

YouTube : [@oussamadallel5](https://www.youtube.com/@oussamadallel5)

LinkedIn : [Oussama Dallel](https://www.linkedin.com/in/oussama-dallel-120143209/)

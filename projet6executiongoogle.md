#Exercice 6: Crontab

#Le script doit exécuter google.com avec curl
#Journaliser l'exécution du fichier 
#tester avec tail -f pour voir en temps réel les logs
#voici les etapes:

#1. Création d'un fichier
touch google.log

#2. creation d'un fichier script avec nano
curl -s "http://www.google.com" >> /home/ec2-user/google.log

#3. Journalisation de l'exécution du fichier
crontab -e
* * * * * /home/ec2-user/googl.sh

#4.tester avec tail -f pour voir en temps réel les logs
tail -n 1  -f google.log


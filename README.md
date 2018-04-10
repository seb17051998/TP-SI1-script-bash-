# TP-SI1-script-bash-
Script bash effectué en si1 en 1ère année de bts sio 

L'exercice 1 est un exercice ou on doit saisir les 4 octets d'une adresse ip et l'afficher.

```
#!/bin/sh
echo "entrer le 1er octet d'une adresse IP." 
read octet1
echo "entrer le 2ème octet d'une adresse IP."
read octet2
echo "entrer le 3ème octet d'une adresse IP."
read octet3
echo "entrer le 4ème octet d'une adresse IP."
read octet4

echo "octet1 :$octet1 octet2 :$octet2 octet3 :$octet3 octet4 :$octet4"
echo "L'adresse IP est $octet1.$octet2.$octet3.$octet4"

```

L'exercice 2 permet de calculer un nombre saisit par l'utilisateur au carré et au cube.

```

#!/bin/sh
echo saisir un nombre entier x
read x
n=$((x*x))
ncube=$((x*x*x))
echo Voici le carré de ce nombre: $n
echo Voici le cube de ce nombre: $ncube

```
L'exercice 3 permet de saisir et de vérifier si l'octet d'une adresse ip dépasse pas 255 sinon on lui envoie un message d'erreur. Si tout les 4 sont ok alors on ping cette adresse ip. 

```
#!/bin/sh

echo "Entrer le 1er octet d'une adresse ip"
read val1

echo "Entrer le 2eme octet d'une adresse ip"
read val2

echo "Entrer le 3eme octet d'une adresse ip"
read val3

echo "Entrer le 4eme octet d'une adresse ip"
read val4

nb=255
if [ $val1 -le $nb ]
	then echo "Octet1:$val1 OK"
	else echo "Octet1:$val1 Incorrect"
fi
if [ $val2 -le $nb ]
	then echo "Octet2:$val2 OK"
	else echo "Octet2:$val2 Incorrect"
fi
if [ $val3 -le $nb ]
        then echo "Octet3:$val3 OK"
        else echo "Octet3:$val3 Incorrect"
fi
if [ $val4 -le $nb ]
        then echo "Octet4:$val4 OK"
        else echo "Octet4:$val4 Incorrect"
fi

ping $val1.$val2.$val3.$val4
```

# Festivallen

Voor veel festivals hebben we veel werknemers nodig die op verschillende locaties werken.
Hiervoor heb ik een Festival-API gemaakt die het makkelijk maakt om users te koppelen aan festival en locaties aan festivals.

#Authenticatie GET & POST users

Als eerste maken we een gebruiker aan met de POST user. Hier kunnen we de gegevens van de werknemer toevoegen die nodig zijn om het te koppelen aan een festival.

Als we een werknemer terug willen vinden gebruiken we de GET user. Hieronder bevindt zich de GET van de users die aangemaakt zijn voor de authenticatie.
![image](https://github.com/bervoetshannes/API-python/assets/47882529/aef80b93-e170-4717-9485-9080f7e9b322)
Met behulp van skip en limit kunnen en we een exact aantal users laten zien.
Zelf heb ik een extra parameter active erbij gestoken voor het kijken of de gebruiker nog actief is.

#POST Locatie

Elk Festival zit op één bepaalde locatie, maar dit wilt niet zeggen dat elke locatie maar één festival heeft.
Daarom is het belangrijk om eerst de locaties aan te maken voordat een festival aangemaakt kan worden.
Bij een Locatie geven we 3 parameters terug: naam, lat en lon. 
De naam voor te weten hoe de locatie heet en de lat en lon voor de coördinatie van de locatie.

#POST Festival
Bij het aanmaken van een festival hebben we 2 parameters: de naam van het festival en de locatie_id
We hebben hier alleen maar de id van de locatie nodig voor het terugkoppelen naar de andere gegevens
Hiervoor hebben we 2 classes voor festival, één voor de POST en één voor de GET.


#DELETE Festival
Als er een festival afgezegd wordt willen we deze verwijderen uit onze db. 
We doen dit niet voor locaties omdat deze toch niet zomaar verdwijnen.

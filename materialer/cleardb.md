<!-- JS use if these pages are used as githubpages. can be deleted if used elsewhere -->
<script src="https://code.jquery.com/jquery-3.2.1.min.js"></script>
<script src="../script.js"></script> 


# Tutorial: ClearDB og Heroku deployment

ClearDB er en mysql database management system, som kan tilkøbes hos Heroku. Den mindste version er gratis. Det følgende er en beskrivelse af hvordan i tilkøber den på Heroku og hvordan i bruger den i jeres Spring Boot projekter. 

## Kreditkort
Selvom den database i skal bruge som udgangspunkt er gratis skal i for at få lov til at bruge den tilknytte et kreditkort til jeres konto på Heroku. 
Klik på brugericonet øverst i højre hjørne. Vælg derefter "Account settings" og "billing". Indtast jeres kreditkortoplysninger.   

**Note:** Selvom i formegentligt ikke kommer til at betale noget for brugen af jeres tilkyttede database, kan jeg ikke garanterer at i ikke kommer til det! 


## Tilføj ClearDB til jeres app på Heroku
I kan nu under menupunktet "Resources" tilføje add-ons.

![](../img/cleardb_addon.png) 

Skriv clear, og klik på "ClearDB".     

I den dropdown der kommer op har i nu mulighed for at vælge forskellige versioner.     

Vælg "Ignite" og klik på "Submit order form".

![](../img/submit_order_form.png)



 

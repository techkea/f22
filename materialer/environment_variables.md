<!-- JS use if these pages are used as githubpages. can be deleted if used elsewhere -->
<script src="https://code.jquery.com/jquery-3.2.1.min.js"></script>
<script src="../script.js"></script> 

# Forbindelse til databasen gennem miljøvariabler
Indtil videre har i brugt jeres application.properties fil til at "holde" informationer vedrørende jeres database.

I denne tutorial skal lærer i hvordan i opsætter og bruger miljøvariabler istedet for application.properties metoden, som i har brugt indtil nu. 

## Problemet som vi gerne vil løse 
Når i skriver brugernavn og password ind i application.properties filen bliver i nød til at gøre denne fil tilgængelig for jeres applikation på Heroku. Det betyder at denne fil bliver nød til at ligge på Github (i hvert tilfælde når vi bruger den deployment metode som vi har brugt i undervisningen dette semester.).    

Problemet med denne metode er at alle i hele verden vil kunne se jeres brugernavn og password (da i sikkert bruger et public repository).    

### Private repository
En løsning er at gøre jeres github repository "private", men det kan give problemer i forhold til colaborators og andre der skal se jeres kode (din lære f.eks).     

### Environment variabler (miljøvariabler)
En anden mere holdbar løsning er at slette indholdet i application.properties og så istedet skrive username og password et andet sted end i selve spring boot projektet. Dette kan gøre i din computers miljøvariabler (og på computeren hos Heroku´s miljøvariabler)

Det følgende er en beskrivelse af hvordan du gør dette. 

## Lokalt på din egen computer

Åben din Spring Boot Web App i Intellij.  Slet alt indhold i din application.properties fil. klik herefter på:

````
	Run -> Edit configurations -> Environment -> Environment Variables
```` 
Dette åbner en Gui som denne.    

![](materialer/env_1.png)

````
	 try (InputStream input = new FileInputStream("src/main/resources/application.properties")) {
            Properties properties = new Properties();
            properties.load(input);
            url = properties.getProperty("url");
            user = properties.getProperty("user");
            password = properties.getProperty("password");
        } catch (IOException ex) {
            ex.printStackTrace();
        }
````

Skal ændres til dette:    


````
	url = System.getenv("url"); 
        user = System.getenv("mp_user"); 
        password = System.getenv("mp_password"); 

````


Den fulde url kommer derfor til at se sådan ud:
````
	mysql://b270aec8833o9i:f6015344@eu-cdbr-west-01.cleardb.com/heroku_cf41053fe067y7r?reconnect=true&autoReconnect=true 
````

#### application.properties 
application.properties for denne database vil derfor se således ud:

```` 
	user=b270aec8833o9i
	password=f6015344
	url=jdbc:mysql://eu-cdbr-west-01.cleardb.com/heroku_cf41053fe067y7r?reconnect=true&autoReconnect=true
```` 

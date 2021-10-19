<script src="https://code.jquery.com/jquery-3.2.1.min.js"></script>
<script src="script.js"></script>

<div style="text-align:right"><small>
Undervisning: Dat21v2 onsdage 08:30 - 11:45 <br>    
Undervisning: Dat21v1 fredage 12:30 - 15:45 <br>    
Underviser: Claus Bove, clbo@kea.dk <br>
<br><br>
</small>  
</div>

| Dat21v2 | Dat21v1 | Emne | 
|:---|:---| --- |
||| [Introduktion til Teknologifaget, OS og CLI ](1.md)|
||| [Databaser](2.md)|
||| [Versionsstyrring (git)](3.md)|
||| [Git branches, merge og merge conflicts](4.md)|
||| [Projektsamarbejde med git og github](5.md)|
||| [Obligatorisk opgave (git & github)](6.md)|
||| [Deployment med Github, Heroku ](7.md)|
||| | 
||| [Deployment med Github, Heroku og Dreamhost](8.md)|
||| [Client / Server Arkitektur](10.md) |
||| [Miniprojekt](11.md)|
||| [Miniprojekt](12.md)|
||| [Repetition og "Klar til eksamensprojektet"](13.md)|
||| [Eksamensprojekt](14.md)|
||| [Eksamensprojekt](15.md)|
||| [Eksamensprojekt](16.md)|

<br><br>
<div style='text-align:right'><i><small>* undervisning på Teams</small></i></div>
<div style='text-align:right'><i><small>** ingen undervisning, starten på jeres miniprojekt</small></i></div>

<script>  
var dates = [
	{dat21v2: '25/08', dat21v1: '27/08'},
	{dat21v2: '01/09', dat21v1:'03/09' },
	{dat21v2: '08/09*', dat21v1:'10/09' },
	{dat21v2: '15/09', dat21v1:'17/09' 	},
	{dat21v2: '22/09*', dat21v1:'24/09'},
	{dat21v2: '29/09', dat21v1:'01/10'  },
	{dat21v2: '06/10*', dat21v1:'08/10'  },
	{dat21v2: '13/10', dat21v1:'15/10' },

	{dat21v2:'20/10*', dat21v1:'22/10' },

	{dat21v2:'27/10', dat21v1:'29/10'},
	{dat21v2:'03/11**', dat21v1:'05/11'},
	{dat21v2:'10/11', dat21v1:'12/11'},
	{dat21v2:'17/11*', dat21v1:'19/11'},
	{dat21v2:'24/11', dat21v1:'26/11'},
	{dat21v2:'01/12*', dat21v1:'03/12' },
	{dat21v2:'08/12', dat21v1:'10/12'},

]
var table = document.getElementsByTagName("table");  
var tbody = document.getElementsByTagName("tbody")
var rows = document.getElementsByTagName("tr");  
for(i = 1; i < rows.length; i++){  
  var tds = rows[i].getElementsByTagName("td"); 
  tds[0].innerHTML= dates[i-1].dat21v2; 
  tds[1].innerHTML= dates[i-1].dat21v1;
}
/*
var section = document.getElementById('downloads');
console.log(section)
var ar = section.getElementsByTagName("a");

for (i = 0; i < ar.length; ++i)
   ar[i].style.display = "none";
*/

</script>

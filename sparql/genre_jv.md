> requête pour récupérer la liste des genre de jeux vidéo existant sur Wikidata.  

```
PREFIX wd: <http://www.wikidata.org/entity/>
PREFIX wdt: <http://www.wikidata.org/prop/direct/>

select distinct ?genreLabel
where
{ ?jeu wdt:P31 wd:Q7889.
  ?jeu wdt:P136 ?genre.
 
 SERVICE wikibase:label{
   bd:serviceParam wikibase:language "en"
                   }
 }
```

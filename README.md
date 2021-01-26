# SUITE DE L'EXERCICE

## Liste des fromages français
'''
<p color="red">Ce jeu de données réunit la liste de 338 spécialités de fromages françaises.Il comprend : le nom du fromage, le département de fabrication, l'URL de la page Wikipédia française, l'URL de la page Wikipédia anglaise quand elle existait, la photographie quand elle existait, les coordonnées géographiques du département de fabrication, Identifiant du jeu de données: fromagescsv-fromagescsv@public.com</p>

<p align="center"><iframe frameborder="0" width="800" height="600" src="https://data.opendatasoft.com/map/embed/filtre_en_polygone/?&static=false&scrollWheelZoom=false"></iframe>)</p>
<iframe src="https://data.opendatasoft.com/chart/embed/camembert0/?&static=false&datasetcard=false" width="400" height="300" frameborder="0"></iframe>
<iframe src="https://data.opendatasoft.com/chart/embed/radar/?&static=false&datasetcard=false" width="400" height="300" frameborder="0"></iframe>

'''sparql
## Requête permettant d'afficher la liste des identifiants des peintures de Monet et ses lieux de conservation
'''
SELECT ?painting ?paintingLabel ?image WHERE {
  ?painting wdt:P31 wd:Q3305213;
    wdt:P170 wd:Q296;
    wdt:P18 ?image;
    wdt:P195 ?lieu.
  SERVICE wikibase:label { bd:serviceParam wikibase:language "en". }
}
'''
## Requête permettant d'afficher la grille d’images des lions
'''
SELECT ?item ?itemLabel ?image WHERE {
  ?item wdt:P31 wd:Q140.
  OPTIONAL { ?item wdt:P18 ?image. }
  SERVICE wikibase:label { bd:serviceParam wikibase:language "en". }
}

'''
## Par ordre descendant
'''
SELECT ?painting ?paintingLabel ?image WHERE {
  ?painting wdt:P31 wd:Q3305213;
    wdt:P170 wd:Q296;
    wdt:P18 ?image;
    wdt:P195 ?lieu.
  SERVICE wikibase:label { bd:serviceParam wikibase:language "en". }
}
ORDER BY DESC(?sitelinks) 
'''

## Requête peremettant d'afficher les lieux où sont conservées des peintures/(nombre de peinture?)

Instances of abusive, harassing, or otherwise unacceptable behavior may be
reported by contacting the project team at alexeykhr@outlook.com. All
complaints will be reviewed and investigated and will result in a response that
is deemed necessary and appropriate to the circumstances. The project team is
obligated to maintain confidentiality with regard to the reporter of an incident.
Further details of specific enforcement policies may be posted separately.

Project maintainers who do not follow or enforce the Code of Conduct in good
faith may face temporary or permanent repercussions as determined by other
members of the project's leadership.


[homepage]: https://www.contributor-covenant.org

For answers to common questions about this code of conduct, see
[https://www.contributor-covenant.org/faq](https://www.contributor-covenant.org/faq)

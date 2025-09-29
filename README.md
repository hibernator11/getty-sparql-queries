## Getty provenance index
This repository intends to describe examples of SPARQL queries for the [Provenance Index](https://data.getty.edu/provenance/docs/) at Getty. The SPARQL point is available at https://data.getty.edu/provenance/sparql-ui.

### Retrieve all classes

```
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
SELECT distinct ?class WHERE {
  ?sub rdf:type ?class .
} LIMIT 100
```


### Retrieve places using Getty identifiers
```
PREFIX skos: <http://www.w3.org/2004/02/skos/core#>
PREFIX owl: <http://www.w3.org/2002/07/owl#>
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
SELECT ?getty ?label WHERE {
  ?sub rdf:type <http://www.cidoc-crm.org/cidoc-crm/E53_Place> .
  ?sub skos:exactMatch ?getty .
  ?sub rdfs:label ?label
} LIMIT 200
```

### Licence
<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Licence Creative Commons" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/80x15.png" /></a><br />Content is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International license</a>.

Please, note that the datasets used in this project have separate licences.

### References
- https://www.moma.org/collection/provenance/
- https://www.getty.edu/projects/getty-provenance-index-initiative/research-inspired-by-the-getty-provenance-index/
- https://www.getty.edu/databases-tools-and-technologies/provenance/
- https://vocab.getty.edu/tgn/

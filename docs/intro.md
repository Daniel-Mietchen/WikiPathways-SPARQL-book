# Introduction

WikiPathways is a biological pathway database and describes the interactions between
biochemical entities in biological processes [<a href="#citeref1">1</a>,<a href="#citeref2">2</a>,<a href="#citeref3">3</a>,<a href="#citeref4">4</a>].
It can be downloaded and used in various formats, one of which is the Resource
Description Framework (RDF) [<a href="#citeref5">5</a>].

## Metadata queries

**SPARQL** [sparql/metadata.rq](sparql/metadata.code.html)
```sparql
PREFIX dcterms: <http://purl.org/dc/terms/>
PREFIX void:    <http://rdfs.org/ns/void#>
PREFIX pav:     <http://purl.org/pav/>
select distinct ?dataset (str(?titleLit) as ?title) ?date ?license where {
  ?dataset a void:Dataset ;
    dcterms:title ?titleLit ;
    dcterms:license ?license ;
    pav:createdOn ?date .
}
```

Which gives as output:

<table>
  <tr>
    <td><b>dataset</b></td>
    <td><b>title</b></td>
    <td><b>date</b></td>
    <td><b>license</b></td>
  </tr>
  <tr>
    <td>http://data.wikipathways.org/20191110/rdf/</td>
    <td>WikiPathways RDF 20191110</td>
    <td>2019-11-10T10:49:50.340Z</td>
    <td>http://creativecommons.org/publicdomain/zero/1.0/</td>
  </tr>
</table>

## References

1. <a name="citeref1"></a>Pico AR, Kelder T, van Iersel MP, Hanspers K, Conklin BR, Evelo CT. WikiPathways: pathway editing for the people. PLoS Biol. 2008 Jul 22;6(7):e184.  doi:[10.1371/JOURNAL.PBIO.0060184](https://doi.org/10.1371/JOURNAL.PBIO.0060184) ([Scholia](https://tools.wmflabs.org/scholia/doi/10.1371/JOURNAL.PBIO.0060184))
2. <a name="citeref2"></a>Kelder T, van Iersel MP, Hanspers K, Summer-Kutmon M, Conklin BR, Evelo CT, et al. WikiPathways: building research communities on biological pathways. NAR. 2012 Jan;40(Database issue):D1301-7.  doi:[10.1093/NAR/GKR1074](https://doi.org/10.1093/NAR/GKR1074) ([Scholia](https://tools.wmflabs.org/scholia/doi/10.1093/NAR/GKR1074))
3. <a name="citeref3"></a>Summer-Kutmon M, Riutta A, Nunes N, Hanspers K, Willighagen E, Bohler A, et al. WikiPathways: capturing the full diversity of pathway knowledge. NAR. 2016 Jan 4;44(D1):D488-94.  doi:[10.1093/NAR/GKV1024](https://doi.org/10.1093/NAR/GKV1024) ([Scholia](https://tools.wmflabs.org/scholia/doi/10.1093/NAR/GKV1024))
4. <a name="citeref4"></a>Slenter DN, Slenter DN, Kutmon M, Hanspers K, Hanspers K, Riutta A, et al. WikiPathways: a multifaceted pathway database bridging metabolomics to other omics research. NAR. 2018 Jan 4;46(D1):D661–D667.  doi:[10.1093/NAR/GKX1064](https://doi.org/10.1093/NAR/GKX1064) ([Scholia](https://tools.wmflabs.org/scholia/doi/10.1093/NAR/GKX1064))
5. <a name="citeref5"></a>Waagmeester A, Summer-Kutmon M, Riutta A, Miller R, Willighagen E, Evelo CT, et al. Using the Semantic Web for Rapid Integration of WikiPathways with Other Biological Online Data Resources. PLoS Comput Biol. 2016 Jun;12(6):e1004989.  doi:[10.1371/JOURNAL.PCBI.1004989](https://doi.org/10.1371/JOURNAL.PCBI.1004989) ([Scholia](https://tools.wmflabs.org/scholia/doi/10.1371/JOURNAL.PCBI.1004989))



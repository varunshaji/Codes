Codes
=======

The Bigdata graph test code for provenance graph done.

The provenance.properties contain the prpoperty for the journal based approach
and the cluster.config contain properties for the cluster based ocnfiguration.

The query i used to test the provenance is

prefix sc:<http://www.ibsplc.com/sprout/social/2013/01/social#> 
construct { ?a ?b ?c }
where{ 
{ GRAPH ?sid {?a ?b ?c } 
  ?sid sc:source ?p . 
  ?p rdf:type sc:Person . 
  ?p sc:username "varun.k" . } 
}

however this runs in journal model and not in cluster mode!




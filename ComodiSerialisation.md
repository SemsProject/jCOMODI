Serialisations of [COMODI](http://sems.uni-rostock.de/trac/wiki/comodi/wiki) annotations in jCOMODI 
===================================================================================================

RDF/XML 
-------

example of an [RDF/XML](http://www.w3.org/TR/rdf-syntax-grammar/) annotation:

```xml
<rdf:RDF
    xmlns:comodi="http://purl.org/net/comodi#"
    xmlns:rdf="http://www.w3.org/1999/02/22-rdf-syntax-ns#">
  <comodi:Change rdf:about="file://bives.patch#25">
    <comodi:affects rdf:resource="http://purl.org/net/comodi#Kinetics"/>
    <comodi:affects rdf:resource="http://purl.org/net/comodi#ParameterDefinition"/>
    <comodi:hasReason rdf:resource="http://purl.org/net/comodi#ModelCuration"/>
    <comodi:hasChangeType rdf:resource="http://purl.org/net/comodi#Move"/>
    <comodi:hasIntention rdf:resource="http://purl.org/net/comodi#Correction"/>
    <comodi:appliesTo rdf:resource="http://purl.org/net/comodi#Node"/>
  </comodi:Change>
</rdf:RDF>
```

TURTLE 
-------

example of an annotation in [TURTLE](https://en.wikipedia.org/wiki/Turtle_%28syntax%29) format

```turtle
@prefix rdf:   <http://www.w3.org/1999/02/22-rdf-syntax-ns#> .
@prefix comodi: <http://purl.org/net/comodi#> .

<file://bives.patch#25>
        a                     comodi:Change ;
        comodi:affects        comodi:Kinetics , comodi:ParameterDefinition ;
        comodi:appliesTo      comodi:Node ;
        comodi:hasChangeType  comodi:Move ;
        comodi:hasIntention   comodi:Correction ;
        comodi:hasReason      comodi:ModelCuration .
```
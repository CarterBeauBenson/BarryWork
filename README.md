<rdf:RDF xmlns:rdf="http://www.w3.org/1999/02/22-rdf-syntax-ns#"
         xmlns:owl="http://www.w3.org/2002/07/owl#"
         xmlns:rdfs="http://www.w3.org/2000/01/rdf-schema#"
         xmlns:xsd="http://www.w3.org/2001/XMLSchema#"
         xmlns:naics="http://example.com/naics/">

    <owl:Ontology rdf:about="http://example.com/naics.owl"/>

    <owl:Class rdf:about="#Sector">
        <rdfs:subClassOf rdf:resource="http://www.w3.org/2004/02/skos/core#Concept"/>
    </owl:Class>

    <owl:Class rdf:about="#Subsector">
        <rdfs:subClassOf rdf:resource="#Sector"/>
    </owl:Class>

    <owl:Class rdf:about="#IndustryGroup">
        <rdfs:subClassOf rdf:resource="#Subsector"/>
    </owl:Class>

    <owl:Class rdf:about="#Industry">
        <rdfs:subClassOf rdf:resource="#IndustryGroup"/>
    </owl:Class>

    <!-- Sector 11 - Agriculture, Forestry, Fishing and Hunting -->
    <owl:NamedIndividual rdf:about="#AgricultureForestryFishingAndHunting">
        <rdf:type rdf:resource="#Sector"/>
        <rdfs:label>Agriculture, Forestry, Fishing and Hunting</rdfs:label>
        <naics:code>11</naics:code>
    </owl:NamedIndividual>

    <!-- Subsector 111 - Crop Production -->
    <owl:NamedIndividual rdf:about="#CropProduction">
        <rdf:type rdf:resource="#Subsector"/>
        <rdfs:label>Crop Production</rdfs:label>
        <naics:code>111</naics:code>
        <rdfs:subClassOf rdf:resource="#AgricultureForestryFishingAndHunting"/>
    </owl:NamedIndividual>

    <!-- Subsector 112 - Animal Production and Aquaculture -->
    <owl:NamedIndividual rdf:about="#AnimalProductionAndAquaculture">
        <rdf:type rdf:resource="#Subsector"/>
        <rdfs:label>Animal Production and Aquaculture</rdfs:label>
        <naics:code>112</naics:code>
        <rdfs:subClassOf rdf:resource="#AgricultureForestryFishingAndHunting"/>
    </owl:NamedIndividual>

    <!-- Industry Group 1124 - Sheep and Goat Farming -->
    <owl:NamedIndividual rdf:about="#SheepAndGoatFarming">
        <rdf:type rdf:resource="#IndustryGroup"/>
        <rdfs:label>Sheep and Goat Farming</rdfs:label>
        <naics:code>1124</naics:code>
        <rdfs:subClassOf rdf:resource="#AnimalProductionAndAquaculture"/>
    </owl:NamedIndividual>

    <!-- Industry Group 1125 - Aquaculture -->
    <owl:NamedIndividual rdf:about="#Aquaculture">
        <rdf:type rdf:resource="#IndustryGroup"/>
        <rdfs:label>Aquaculture</rdfs:label>
       

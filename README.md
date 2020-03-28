# OntoExpLine
An Ontology for Experiment Lines.

## Overview

This repository presents a guide for OntoExpLine, an ontology for experiment lines, which give support to scientists to derive workflows that are composed of variant programs that implement the same activity on the flow.
Using OntoExpLine is possible to relate different kind of data and provenance, and apply reasoners mechanisms to query data used to create the scientific experiment and the data product generated during the experiment execution. OntoExpLine is composed of four specific modules: workflow structure, experiment line, domain-data branch, and metadata block.


## Introduction

Scientific experiments involve several combinations of data and abstract activities on the flow. Besides this, there are many equivalences in the workflow construct process because different concrete programs can implement an abstract activity, and these programs can consume and generate different resources. However necessary, derive workflows is an intricate work because abstract tasks, concrete programs, and their compatibilities should be defined and connected to compose the flow variations. Based on this, apply formal models in this context can help scientists to derive the workflow in an experiment line set. This kind of model gives support to scientists to realize different kinds of verifications to confirm or refute a scientific hypothesis, applying mechanisms such as reasoners and inference languages. 

Another characteristic that ontologies apply in the workflow derivation context is related to link different data types.  This way, domain data, prospective and retrospective provenance, and metadata annotations can be aggregated to the workflow specification. This possibility impact on the reproducibility and experiment reuse, because it helps other scientists reply the same experience and achieve datasets compatible with the originals.

Based on the above, this page presents OntoExpLine, a model for Experiment Lines that aims to support experiments derivation processes.  OntoExpLine is the result of the integration of task ontologies ( [ProveONE][1] and [Experiment Line][2]), domain ontology branch ([EDAM][3]), and [Dublin Core classes][4], to improve data products about the task and domain concepts.

## OntoExpLine Conceptual Model 
(esquema de relacionamentos das classes)
## OntoExpLine Specification
(descrição das classes - has super-class, is in domain of, is in range of - examplos de funcionamento)

## References

[1] http://jenkins-1.dataone.org/jenkins/view/Documentation%20Projects/job/ProvONE-Documentation-trunk/ws/provenance/ProvONE/v1/provone.html
[2] https://link.springer.com/chapter/10.1007/978-3-642-02279-1_20
[3] http://edamontology.org/page
[4] https://dublincore.org/

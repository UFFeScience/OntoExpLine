# OntoExpLine
An Ontology for Experiment Lines.

## Overview

This repository presents a guide for OntoExpLine, an ontology for experiment lines, which give support to scientists to derive workflows that are composed of variant programs that implement the same activity on the flow.
Using OntoExpLine is possible to relate different kind of data and provenance, and apply reasoners mechanisms to query data used to create the scientific experiment and the data product generated during the experiment execution. OntoExpLine is composed of four specific modules: workflow structure, experiment line, domain-data branch, and metadata block.


## Introduction

Scientific experiments involve several combinations of data and abstract activities on the flow. Besides this, there are many equivalences in the workflow construct process because different concrete programs can implement an abstract activity, and these programs can consume and generate different resources. However necessary, derive workflows is an intricate work because abstract tasks, concrete programs, and their compatibilities should be defined and connected to compose the flow variations. Based on this, apply formal models in this context can help scientists to derive the workflow in an experiment line set. This kind of model gives support to scientists to realize different kinds of verifications to confirm or refute a scientific hypothesis, applying mechanisms such as reasoners and inference languages. 

Another characteristic that ontologies apply in the workflow derivation context is related to link different data types.  This way, domain data, prospective and retrospective provenance, and metadata annotations can be aggregated to the workflow specification. This possibility impact on the reproducibility and experiment reuse, because it helps other scientists reply the same experience and achieve datasets compatible with the originals.

Based on the above, this page presents OntoExpLine, a model for Experiment Lines that aims to support experiments derivation processes.  OntoExpLine is the result of the integration of task ontologies: [ProveONE][1] and [Experiment Line][2]; domain ontology branch: [EDAM][3]; and [Dublin Core classes][4], to improve data products about the task and domain concepts.

## OntoExpLine Conceptual Model 

This section introduces OntoExpLine on a diagram representing its conceptual model. As mentioned previously the OntoExpLine is the integration of four ontologies. This way the components and their relations are the same that the original ones. The conceptual modeling is shown in Figure 1. 

![OntoExpLine structure](https://github.com/UFFeScience/OntoExpLine/blob/master/img/ontoexpline.png)*Figure 1, OntoExpLine Structure.*

The ProveONE module is composed of three blocks that are used to link trace, workflow, and data instances.  The __trace representation__ components are responsible for aggregate execution data related to agents (such as users and software components), and resource usage. The __workflow representation__ block is composed of modules to describe and specify the workflow structure (such as programs, ports, and controllers).  On the other hand, the __data representation__ module aims to describe and relate the data instances consumed and produced during the workflow execution. The properties used to link the data instances are described in Table 1.

| Property | Domain | Range | Usage Example|
|---|---|---|---|
| provone:hasSubProgram | Program | Program |Program p1 *hasSubProgram* p3|
| provone:controlledBy | Program | Controller | Program p1 *controlledBy* p2|
| provone:controls | Controller | Program | Controller p2 *controls* p3|
| provone:hasInPort	 | Program |  Port |  Program p1 *hasInPort* inp1 | 
| provone:hasOutPort |  Program |  Port |   Program p1 *hasOutPort* outp1| 
| provone:hasDefaultParam |  Port |  Entity |  Port inp1 *hasDefaultParam* data1 | 
| provone:connectsTo |  Port |  Channel |  Port inp1 *connectsTo* ch1 | 
| provone:wasDerivedFrom |  Program, Workflow |  Program, Workflow |  Program p4 *wasDerivedFrom* p1 | 
| provone:used |  Execution |  Entity |  Execution p1ex1 *used* data1 | 
| provone:wasGeneratedBy |  Entity |  Execution |  Entity data2 *wasGeneratedBy* p1ex1| 
| provone:wasAssociatedWith |  Execution |  User |  Execution p1ex1 *wasAssociatedWith* userXQD| 
| provone:wasInformedBy |  Execution |  Execution |  Execution p1ex2 *wasInformedBy* p1ex1 | 
| provone:wasPartOf |  Execution |  Execution |  Execution p1ex2 *wasPartOf* p| 
| provone:qualifiedAssociation |  Execution |  Association |  Execution pex1 *qualifiedAssociation* userXQD | 
| provone:agent |  Association |  User |   Association assoc1 *agent* userXQD| 
| provone:hadPlan |  Association |  program |  Association assoc1 *hadPlan* p1| 
| provone:qualifiedUsage |  Execution |  Usage |  Execution pex2 *qualifiedUsage* data2 | 
| provone:hadInPort |  Usage |  Port |  Usage usage1 *hadInPort* inp1 | 
| provone:hadEntity |  Usage, Generation |  Entity |   Usage usage1 *hadEntity* data1| 
| provone:qualifiedGeneration |  Execution | Generation |  Execution p1exe1 *qualifiedGeneration* ent1| 
| provone:hadOutPort |  Generation |  Port |   Execution p1exe1 *hadOutPort* outp1| 
| provone:hadMember |  Collection |  Entity |  Collection C1 *hadMember* E1 | 

## OntoExpLine Specification
(descrição das classes - has super-class, is in domain of, is in range of - examplos de funcionamento)



[1]:http://jenkins-1.dataone.org/jenkins/view/Documentation%20Projects/job/ProvONE-Documentation-trunk/ws/provenance/ProvONE/v1/provone.html

[2]:https://link.springer.com/chapter/10.1007/978-3-642-02279-1_20

[3]:http://edamontology.org/page

[4]:https://dublincore.org/

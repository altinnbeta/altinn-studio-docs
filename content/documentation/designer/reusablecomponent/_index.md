---
title: Creating Reusable resources
linktitle: Reusable Resources
description: The UI-designer is the part of Altinn Studio where the service developer can create
tags: ["tjenester 3.0"]
weight: 106
---

{{<figure src="formdesigner1.png?width=1000" title="Definering av layout for tjenesten \"Starte Enkeltpersonforetak\"">}}



### Create reusable resources

A important feature with Altinn Studio is that it should promote developers to create
reusable resources that can be reused by other service developers that uses Altinn Studio.

Reusable resource is typical created by technical developers using code editors.

{{<figure src="../react-code-example.png?width=1000" title="Development of new React web component">}}

#### Web component

When [building UI](#building-ui), you will use and configure premade web components.
The components will be based on [React](https://reactjs.org/), and vil vary in size
and complexity. Web components are developed in code editors.

Some basic requirements:

- The component should be flexible and configurable
- The component should be able to be connected to the data model, and use the metadata from the data model.
- The component should be able to connect to text resources
- The component should support responsive design and WCAG 2 AA
- It should be simple for service owners to add more components

![React logo](../react-icon.svg?width=100)

#### Overall layout

When [building UI](#bygge-brukergrensesnitt) it will be possible to select a overall layout 
 (aka "look&feel"). 
This could bee neded because of the complexity of the service or a wish for branding of the service.


- Create reuasable artifacts

  - Look&feel
  - Texts and translations
  - Code lists
  - Logic (C#? TypeScript? WebAssembly?)
  - Data models (Seres?)
  - API calls
- Reuse these artifacts

F.eks. det å lage nye web componenter og layouts vil typisk være noe som 
tekniske utviklere gjør i kode-editorer.  
Det å sette disse sammen og konfigurere dem, er noe alle skal kunne gjøre.


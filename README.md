# Encuentro de profesores de computación 2918

## Recursos Didacticos

* [MermaidJS](https://mermaidjs.github.io/). - Libreria Javascript para generación de Diagramas de flujo utilizando Markdown
* [Gravizo]()- API que permite incrustar diagramas en [GraphViz](),[Dot](),[Mermaid]() en editores Markdown en linea, incluyendo Github
* [Markdown Plus](https://mdp.tylingsoft.com/#preferences-modal). Editor Markdown en linea que permite incluir graficos en GraphViz, Miriad y otros formatos
* [flowcharj.js](). Libreria Javascript para la generación de SVG 
* [GitBook](https://www.gitbook.com/). Documentación de proyectos en Markdown.

## Ejemplos

### Gantt diagram

```mermaid
gantt
dateFormat  YYYY-MM-DD
title Adding GANTT diagram to mermaid

section A section
Completed task            :done,    des1, 2014-01-06,2014-01-08
Active task               :active,  des2, 2014-01-09, 3d
Future task               :         des3, after des2, 5d
Future task2               :         des4, after des3, 5d

section Critical tasks
Completed task in the critical line :crit, done, 2014-01-06,24h
Implement parser and jison          :crit, done, after des1, 2d
Create tests for parser             :crit, active, 3d
Future task in critical line        :crit, 5d
Create tests for renderer           :2d
Add to mermaid                      :1d

section Documentation
Describe gantt syntax               :active, a1, after des1, 3d
Add gantt diagram to demo page      :after a1  , 20h
Add another diagram to demo page    :doc1, after a1  , 48h

section Last section
Describe gantt syntax               :after doc1, 3d
Add gantt diagram to demo page      : 20h
Add another diagram to demo page    : 48h
```



![Alt text](https://g.gravizo.com/svg?
  digraph G {
    aize ="4,4";
    main [shape=box];
    main -> parse [weight=8];
    parse -> execute;
    main -> init [style=dotted];
    main -> cleanup;
    execute -> { make_string; printf}
    init -> make_string;
    edge [color=red];
    main -> printf [style=bold,label="100 times"];
    make_string [label="make a string"];
    node [shape=box,style=filled,color=".7 .3 1.0"];
    execute -> compare;
  }
)

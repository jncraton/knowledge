Ontology
========

A structured representation of knowledge in a domain

Learning Outcomes
-----------------

After completing this lab, student will be able to:

- Describe relationships between statements to form a knowledge grahp
- Represent a graph using graphviz
- Build a small ontology covering a domain of interest

Assignment
----------

Select a domain of interest and create a small, graphical ontology demonstrating how entities in this domain are connected. Here very short example for publications:


You should use graphviz to document your relationships and build a graph. You may use graphviz via the CLI, any GUI you choose, or [free hosted web tools](https://dreampuf.github.io/GraphvizOnline/?engine=dot).

Here is the above graph in graphviz:

```graphviz
digraph G {
    Article -> Publication [label=is]
    Book -> Publication [label=is]
    "Blog Post" -> Publication [label=is]
    
    Publication -> Title [label=has]
    Publication -> Author [label=has]
    Publication -> Pubdate [label=has]

    Author -> Person [label=is]
    Person -> Birthdate [label=has]
    Person -> Name [label=has]
    
    Name -> "Proper Noun" [label=is]
    Title -> "Proper Noun" [label=is]
    
    Pubdate -> Date [label=is]
    Birthdate -> Date [label=is]
    
    Date -> Year [label=has]
    Date -> Month [label=has]
    Date -> Day [label=has]
    
    Month -> "Proper Noun" [label=is]
}
```

Requirements
------------

Your graph should include at least the following:

- 20 entities
- 25 relationships between entities

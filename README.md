# Beyond the Meta: Leveraging Game Design Parameters for Patch-Agnostic Esport Analitics

This git repository contains the resources described in the paper available [here](todo)
These resources aim at enableing future research within Dota 2 to be patch-agnostic.
This can be achieved by utilising the clustered heroes representation instead of Character IDs or other forms of character representation.

## How it works
This repository contains the following resources.
Resource  | Description
--------  | -----------
ability_data  | Contains standartized data about the ability and the ability's owner. This contains the data used for clustering in its raw (unclustered) format.
kmeans_model  | Contains the pickle information for the trained K-Means model. This can be used to import the model in Python as a SciKitLearn KMeans model.
hero_clustered  | Contains the hero representation format to be used. Each entry in this CSV relates to a hero for a given patch (the first two columns indicate which). This representation is built fro the mode of each cluster for the hero's set of abilities.

hero_clustered.csv was designed to allow researchers to "plug-and-play" this character representation into their research.
Simply locate the relevant patch and hero (using the first two columns) within the CSV.
The remaining columns (from 3 onwards) can then be used as it is for a single hero.

## Cite this work
For in-text citations you sould use: `todo`

Bibliography: 
```
todo
```

Bibtex:
```
todo{

}
```

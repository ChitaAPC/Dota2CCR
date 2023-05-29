# Beyond the Meta: Leveraging Game Design Parameters for Patch-Agnostic Esport Analitics

This git repository contains the resources described in the paper available soon. For more information, please check back at a later date when the paper becomes available.
These resources aim at enabling future research within Dota 2 to be patch-agnostic by including contextual information about several (or at least the current).
This can be achieved by utilising the clustered heroes representation instead of Character IDs or other forms of character representation.

## How it works
This repository contains the following resources.
Resource  | Description
--------  | -----------
ability_data  | Contains standartized data about the ability and the ability's owner. This contains the data used for clustering in its raw (unclustered) format.
kmeans_model  | Contains the pickle information for the trained K-Means model. This can be used to import the model in Python as a SciKitLearn KMeans model.
ability_cluster | Contains the cluster for each ability for any given patch (`7.27` onwards). These clusters are used to create the vectors for hero representation.
hero_clustered  | Contains the hero representation format to be used. Each entry in this CSV relates to a hero for a given patch (the first two columns indicate which). This representation is built from the mode of each cluster for the hero's set of abilities.

hero_clustered.csv was designed to allow researchers to "plug-and-play" this character representation into their research.
Simply locate the relevant patch and hero (using the first two columns) within the CSV.
The remaining columns (from 3 onwards) can then be used as it is for a single hero.

Note: This methodology only supports Dota 2 patches from `7.27` onwards. Additionally it may take a few days after a new patch is released for all the data to be processed to support the new patch as well.

## Will this representation change next patch?
This form of hero representation is designed to maintain the meaning and the size of each dimension across patches.
This means that when a new patch comes out, the abilities and the heroes will the undergo the same process to generate the representation for that patch.
There should still be the same number of dimensions (68) and they should all represent the same underlying principles.
This means that once data for the new patch becomes available, you should be able to use the same models with the new CSV without the need to re-train or re-architecture your models.

There is always a chance that Dota will change dramatically, forcing new clusters to be formed.
If this is the case, you would need to re-train your models.
While we don’t expect that will happen in the near future, it is entirely up to Valve how they update their game. 
We will make it clear if that happens, so check this page for information when a new patch is available.

## Cite this work
This work is in the process of being added to arXiv.
Instructions for citation will be added once the paper is available.


For in-text citations you sould use: `tba`

Bibliography: 
```
tba
```

Bibtex:
```
tba{

}
```

# HSGWCR

A system that takes any object as input and recursively breaks it down into a tree of components and subcomponents, all the way down to leaf nodes that no longer need further decomposition.
Each node in the tree is not LLM-generated from memory, but instead grounded in real sources. Wikidata, Wikipedia, and web search are queried first, and the LLM's only job is to extract and structure what the sources actually say.
Every node carries cross-reference metadata, meaning each component must be confirmed by at least 2-3 independent sources before being accepted into the tree. Conflicts between sources are logged, and any node that could not be verified is flagged rather than silently included.
The output is not just a hierarchy. It is a verified, source-cited, confidence-scored component tree where you know exactly how trustworthy each part of the breakdown is.

# Repository structure

The main kinds of files in the repository:

1. Release files
2. Imports
3. [Components](#components)

## Release files
Release file are the file that are considered part of the official ontology release and to be used by the community. A detailed description of the release artefacts can be found [here](https://github.com/INCATools/ontology-development-kit/blob/master/docs/ReleaseArtefacts.md).

## Imports
Imports are subsets of external ontologies that contain terms and axioms you would like to re-use in your ontology. These are considered "external", like dependencies in software development, and are not included in your "base" product, which is the [release artefact](https://github.com/INCATools/ontology-development-kit/blob/master/docs/ReleaseArtefacts.md) which contains only those axioms that you personally maintain.

These are the current imports in UBERON

| Import | URL | Type |
| ------ | --- | ---- |
| pr | https://raw.githubusercontent.com/obophenotype/pro_obo_slim/master/pr_slim.owl | slme |
| cl | http://purl.obolibrary.org/obo/cl.owl | slme |
| go | http://purl.obolibrary.org/obo/go/go-base.owl | slme |
| envo | http://purl.obolibrary.org/obo/envo.owl | slme |
| ro | http://purl.obolibrary.org/obo/ro.owl | slme |
| bspo | http://purl.obolibrary.org/obo/bspo.owl | slme |
| chebi | https://raw.githubusercontent.com/obophenotype/chebi_obo_slim/main/chebi_slim.owl | slme |
| pato | http://purl.obolibrary.org/obo/pato.owl | slme |
| bfo | http://purl.obolibrary.org/obo/bfo.owl | slme |
| ncbitaxon | http://purl.obolibrary.org/obo/ncbitaxon/subsets/taxslim.owl | slme |
| ncbitaxondisjoints | http://purl.obolibrary.org/obo/ncbitaxon/subsets/taxslim-disjoint-over-in-taxon.owl | slme |
| nbo | http://purl.obolibrary.org/obo/nbo.owl | slme |
| orcidio | https://w3id.org/orcidio/orcidio.owl | custom |
| omo | http://purl.obolibrary.org/obo/omo.owl | mirror |
## Components
Components, in contrast to imports, are considered full members of the ontology. This means that any axiom in a component is also included in the ontology base - which means it is considered _native_ to the ontology. While this sounds complicated, consider this: conceptually, no component should be part of more than one ontology. If that seems to be the case, we are most likely talking about an import. Components are often not needed for ontologies, but there are some use cases:

1. There is an automated process that generates and re-generates a part of the ontology
2. A part of the ontology is managed in ROBOT templates
3. The expressivity of the component is higher than the format of the edit file. For example, people still choose to manage their ontology in OBO format (they should not) missing out on a lot of owl features. They may choose to manage logic that is beyond OBO in a specific OWL component.

These are the components in UBERON

| Filename | URL |
| -------- | --- |
| disjoint_union_over.owl | None |
| mappings.owl | None |
| in-subset.owl | None |
| hra_subset.owl | https://raw.githubusercontent.com/hubmapconsortium/ccf-validation-tools/master/owl/UB_ASCTB_subset.owl |
| vasculature_class.owl | None |
| hra_depiction_3d_images.owl | https://raw.githubusercontent.com/hubmapconsortium/ccf-validation-tools/master/owl/hra_uberon_3d_images.owl |

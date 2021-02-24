# NSDR Linked Data API

## Introduction
JSON-LD contexts, Resource Description Framework Schema (RDFS) and JSON schema
documents for the National Soil Data Repository Linked Data API (NSDR-LD).
Schema will be defined to support two API specifications:

1. Documents for JSON-LD resources provided by a JSON:API compliant API (the NSDR default).
2. Schema documents for JSON-LD resources provided by an OGC API - features compliant API (pending).

JSON-LD design decisions are informed by the first and second OGC Environmental
Linked Features Interoperability Experiments (ELFIE and SELFIE).

## Schema purpose and interaction
JSON-LD contexts and RDFS schema are co-dependent. Each JSON-LD context maps JSON
keys onto resources in the RDFS schema. Without an RDFS relation a context is
invalid. Using these contexts and schema, JSON-LD data can be converted into RDF
(e.g. RDF/XML or TTL) and imported into a Semantic Web Triple store.

JSON schema are independent of these but can be used to provided additional
information about the structure and content of documents to parsers that are
JSON schema aware. We anticipate this will the be more common case among client
applications. JSON Schema and RDFS documents should be semantically and
syntactically consistent. The JSON schema will include definitions for JSON-LD
keys (e.g. @context, @id, @type and @value).

## Publication
Schema documents will be published as web resources from:
* https://data.scinfo.org.nz/static/schema/nsdr-ld/

The [MWLR implementation](https://confluence.landcareresearch.co.nz/display/IFX/EISS+Persistent+Identifier+Service)
of the AuScope Persistent Identifier Service will be used to manage the redirects.

## Future work
1. JSON Forms - augment JSON schema with instructions for rendering data in client applications.
2. SHACL integration - full RDF validation support using the Shape Constraint Language.

## References
| What | Where |
| ---- | ----- |
| JSON:API | https://jsonapi.org/format/ |
| JSON-LD | https://www.w3.org/TR/json-ld/ |
| JSON Schema | https://json-schema.org/ |
| OGC ELFIE | https://github.com/opengeospatial/ELFIE |
| OGC SELFIE | https://github.com/opengeospatial/SELFIE |
| RDFS | https://www.w3.org/TR/rdf-schema/ |

## Contact
[Alistair Ritchie](https://github.com/abhritchie)

*Research Data Architect/Engineer*

Informatics Team, Manaaki Whenua Landcare Research

***

[![manaakiwhenua-standards](https://github.com/manaakiwhenua/nsdr-ld/workflows/manaakiwhenua-standards/badge.svg)](https://github.com/manaakiwhenua/manaakiwhenua-standards)
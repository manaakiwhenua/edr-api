# Environmental Data Repository API Schema

## Introduction
JSON Schema, JSON-LD contexts, and Resource Description Framework Schema (RDFS)
documents for the Environmental Data Repository (EDR) JSON and Linked Data API.
Implementations of the EDR (e.g. the National Soils Data Repository) will extend
this base with domain specific schema.

This repository supports two approaches:

1. A JSON API specification compliant API.
2. JSON-LD documents served by a simple, RESTful Linked Data API. The will include
complimentary JSON Schema documents that include definitions for JSON-LD keys
(including @id, @type, @value).

JSON-LD design decisions are informed by the first and second OGC Environmental
Linked Features Interoperability Experiments (ELFIE and SELFIE). This includes
the inclusion of schema.org properties based on the recommendations of
[Science on schema.org](https://science-on-schema.org/).

## Schema purpose and interaction
JSON-LD contexts and RDFS schema are co-dependent. Each JSON-LD context maps JSON
keys onto resources in the RDFS schema. Without an RDFS mapping a context is
invalid. Using these contexts and schema, JSON-LD data can be converted into RDF
(e.g. RDF/XML or TTL) and imported into a Semantic Web Triple store.

JSON schema are independent of these but can be used to provide additional
information about the structure and content of documents to parsers that are
JSON schema aware. We anticipate this will the be more common case among client
applications. For consistency across APIs the JSON Schema and RDFS documents
should be semantically and syntactically consistent.

## Publication
Schema documents will be published as web resources from:
* https://data.scinfo.org.nz/erd/schema/

Apache mod_rewrite and the [MWLR implementation](https://confluence.landcareresearch.co.nz/display/IFX/EISS+Persistent+Identifier+Service)
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
| ESIP Science on schema.org | https://science-on-schema.org/ |

## Contact
[Alistair Ritchie](https://github.com/abhritchie)

*Research Data Architect/Engineer*

Informatics Team, Manaaki Whenua Landcare Research

***

[![manaakiwhenua-standards](https://github.com/manaakiwhenua/nsdr-ld/workflows/manaakiwhenua-standards/badge.svg)](https://github.com/manaakiwhenua/manaakiwhenua-standards)
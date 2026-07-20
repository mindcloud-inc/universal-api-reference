# Rat Genome Database: Native API Reference

A consolidated summary of Rat Genome Database's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://rest.rgd.mcw.edu/rgdws/rgd-api-docs
- **OpenAPI specification:** https://rest.rgd.mcw.edu/rgdws/rgd-api-docs
- **API base URL:** `https://rest.rgd.mcw.edu/rgdws`

## Authentication

### No Authentication

Public REST API with no authentication required.

This API does not require request authentication.

[Official authentication documentation](https://rest.rgd.mcw.edu/rgdws/rgd-api-docs)

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get All Strains](actions/get-all-strains.md) | `GET /strains/all` | [docs](https://rest.rgd.mcw.edu/rgdws/rgd-api-docs) |
| [Get Annotations By RGD ID](actions/get-annotations-by-rgd-id.md) | `GET /annotations/rgdId/:rgdId` | [docs](https://rest.rgd.mcw.edu/rgdws/rgd-api-docs) |
| [Get Annotations For Term](actions/get-annotations-for-term.md) | `GET /annotations/:accId/:speciesTypeKey/:includeChildren` | [docs](https://rest.rgd.mcw.edu/rgdws/rgd-api-docs) |
| [Get Chromosomes By Assembly](actions/get-chromosomes-by-assembly.md) | `GET /maps/chr/:mapKey` | [docs](https://rest.rgd.mcw.edu/rgdws/rgd-api-docs) |
| [Get Chromosomes By Primary Assembly](actions/get-chromosomes-by-primary-assembly.md) | `GET /maps/chrForSpecies/:speciesTypeKey` | [docs](https://rest.rgd.mcw.edu/rgdws/rgd-api-docs) |
| [Get Ensembl Gene Mapping](actions/get-ensembl-gene-mapping.md) | `GET /lookup/id/map/EnsemblGene/:rgdId` | [docs](https://rest.rgd.mcw.edu/rgdws/rgd-api-docs) |
| [Get Gene By RGD ID](actions/get-gene-by-rgd-id.md) | `GET /genes/:rgdId` | [docs](https://rest.rgd.mcw.edu/rgdws/rgd-api-docs) |
| [Get Gene By Symbol](actions/get-gene-by-symbol.md) | `GET /genes/:symbol/:speciesTypeKey` | [docs](https://rest.rgd.mcw.edu/rgdws/rgd-api-docs) |
| [Get Gene Orthologs](actions/get-gene-orthologs.md) | `GET /genes/orthologs/:rgdId` | [docs](https://rest.rgd.mcw.edu/rgdws/rgd-api-docs) |
| [Get Gene Types](actions/get-gene-types.md) | `GET /lookup/geneTypes` | [docs](https://rest.rgd.mcw.edu/rgdws/rgd-api-docs) |
| [Get Genes Annotated](actions/get-genes-annotated.md) | `GET /genes/annotation/:accId/:speciesTypeKey` | [docs](https://rest.rgd.mcw.edu/rgdws/rgd-api-docs) |
| [Get Genes By Keyword](actions/get-genes-by-keyword.md) | `GET /genes/keyword/:keyword/:speciesTypeKey` | [docs](https://rest.rgd.mcw.edu/rgdws/rgd-api-docs) |
| [Get Genes By Species](actions/get-genes-by-species.md) | `GET /genes/species/:speciesTypeKey` | [docs](https://rest.rgd.mcw.edu/rgdws/rgd-api-docs) |
| [Get Genes In Region](actions/get-genes-in-region.md) | `GET /genes/region/:chr/:start/:stop/:mapKey` | [docs](https://rest.rgd.mcw.edu/rgdws/rgd-api-docs) |
| [Get Last News](actions/get-last-news.md) | `GET /news/last` | [docs](https://rest.rgd.mcw.edu/rgdws/rgd-api-docs) |
| [Get Map By Assembly](actions/get-map-by-assembly.md) | `GET /maps/assembly/:mapKey` | [docs](https://rest.rgd.mcw.edu/rgdws/rgd-api-docs) |
| [Get Maps By Species](actions/get-maps-by-species.md) | `GET /maps/:speciesTypeKey` | [docs](https://rest.rgd.mcw.edu/rgdws/rgd-api-docs) |
| [Get NCBI Gene Mapping](actions/get-ncbi-gene-mapping.md) | `GET /lookup/id/map/NCBIGene/:rgdId` | [docs](https://rest.rgd.mcw.edu/rgdws/rgd-api-docs) |
| [Get Phenotype Chart Info](actions/get-phenotype-chart-info.md) | `GET /phenotype/phenominer/chart/:speciesTypeKey/:termString` | [docs](https://rest.rgd.mcw.edu/rgdws/rgd-api-docs) |
| [Get QTL By RGD ID](actions/get-qtl-by-rgd-id.md) | `GET /qtls/:rgdId` | [docs](https://rest.rgd.mcw.edu/rgdws/rgd-api-docs) |
| [Get QTLs By Position](actions/get-qtl-list-by-position.md) | `GET /qtls/:chr/:start/:stop/:mapKey` | [docs](https://rest.rgd.mcw.edu/rgdws/rgd-api-docs) |
| [Get Species Maps Lookup](actions/get-species-maps-lookup.md) | `GET /lookup/maps/:speciesTypeKey` | [docs](https://rest.rgd.mcw.edu/rgdws/rgd-api-docs) |
| [Get Species Types](actions/get-species-types.md) | `GET /lookup/speciesTypeKeys` | [docs](https://rest.rgd.mcw.edu/rgdws/rgd-api-docs) |
| [Get Strain By RGD ID](actions/get-strain-by-rgd-id.md) | `GET /strains/:rgdId` | [docs](https://rest.rgd.mcw.edu/rgdws/rgd-api-docs) |
| [Get Strains By Search Term](actions/get-strains-by-search-term.md) | `GET /strains/search/:term` | [docs](https://rest.rgd.mcw.edu/rgdws/rgd-api-docs) |
| [Get UniProt Mapping](actions/get-uni-prot-mapping.md) | `GET /lookup/id/map/UniProt/:rgdId` | [docs](https://rest.rgd.mcw.edu/rgdws/rgd-api-docs) |
| [Get Variant By RS ID](actions/get-variant-by-rs-id.md) | `GET /variants/:rsId` | [docs](https://rest.rgd.mcw.edu/rgdws/rgd-api-docs) |
| [Get Variants By Position](actions/get-variants-by-position.md) | `GET /variants/:chr/:start/:stop/:mapKey` | [docs](https://rest.rgd.mcw.edu/rgdws/rgd-api-docs) |
| [Get Videos](actions/get-videos.md) | `GET /news/videos` | [docs](https://rest.rgd.mcw.edu/rgdws/rgd-api-docs) |
| [Search Pathways](actions/search-pathways.md) | `GET /pathways/diagrams/search/:searchString` | [docs](https://rest.rgd.mcw.edu/rgdws/rgd-api-docs) |

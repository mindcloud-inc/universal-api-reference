# <img src="https://images.mindcloud.co/apps/icons/rat-genome-database_1776271318386.png" alt="Rat Genome Database logo" width="28" height="28"> Rat Genome Database: Universal API

Search genes, variants, QTLs, and strains

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/ratGenomeDatabase/latest
- **Category:** IT Operations / Database
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://rgd.mcw.edu
- **Vendor API docs:** https://rest.rgd.mcw.edu/rgdws/rgd-api-docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Species Types](actions/get-species-types.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ratGenomeDatabase/latest/actions/get-species-types?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Annotation

| Action | Method | Description |
| --- | --- | --- |
| [Get Annotations By RGD ID](actions/get-annotations-by-rgd-id.md) | GET |  |
| [Get Annotations For Term](actions/get-annotations-for-term.md) | GET |  |

### Chromosome

| Action | Method | Description |
| --- | --- | --- |
| [Get Chromosomes By Assembly](actions/get-chromosomes-by-assembly.md) | GET |  |
| [Get Chromosomes By Primary Assembly](actions/get-chromosomes-by-primary-assembly.md) | GET |  |

### Ensembl Gene Mapping

| Action | Method | Description |
| --- | --- | --- |
| [Get Ensembl Gene Mapping](actions/get-ensembl-gene-mapping.md) | GET |  |

### Gene

| Action | Method | Description |
| --- | --- | --- |
| [Get Gene By RGD ID](actions/get-gene-by-rgd-id.md) | GET |  |
| [Get Gene By Symbol](actions/get-gene-by-symbol.md) | GET |  |
| [Get Gene Orthologs](actions/get-gene-orthologs.md) | GET |  |
| [Get Genes Annotated](actions/get-genes-annotated.md) | GET |  |
| [Get Genes By Keyword](actions/get-genes-by-keyword.md) | GET |  |
| [Get Genes By Species](actions/get-genes-by-species.md) | GET |  |
| [Get Genes In Region](actions/get-genes-in-region.md) | GET |  |

### Gene Type

| Action | Method | Description |
| --- | --- | --- |
| [Get Gene Types](actions/get-gene-types.md) | GET |  |

### Map

| Action | Method | Description |
| --- | --- | --- |
| [Get Map By Assembly](actions/get-map-by-assembly.md) | GET |  |
| [Get Maps By Species](actions/get-maps-by-species.md) | GET |  |
| [Get Species Maps Lookup](actions/get-species-maps-lookup.md) | GET |  |

### Ncbi Gene Mapping

| Action | Method | Description |
| --- | --- | --- |
| [Get NCBI Gene Mapping](actions/get-ncbi-gene-mapping.md) | GET |  |

### News Item

| Action | Method | Description |
| --- | --- | --- |
| [Get Last News](actions/get-last-news.md) | GET |  |

### News Video

| Action | Method | Description |
| --- | --- | --- |
| [Get Videos](actions/get-videos.md) | GET |  |

### Pathway

| Action | Method | Description |
| --- | --- | --- |
| [Search Pathways](actions/search-pathways.md) | GET |  |

### Qtl

| Action | Method | Description |
| --- | --- | --- |
| [Get QTL By RGD ID](actions/get-qtl-by-rgd-id.md) | GET |  |
| [Get QTLs By Position](actions/get-qtl-list-by-position.md) | GET |  |

### Quantitative Phenotype

| Action | Method | Description |
| --- | --- | --- |
| [Get Phenotype Chart Info](actions/get-phenotype-chart-info.md) | GET |  |

### Rat Strain

| Action | Method | Description |
| --- | --- | --- |
| [Get All Strains](actions/get-all-strains.md) | GET |  |
| [Get Strain By RGD ID](actions/get-strain-by-rgd-id.md) | GET |  |
| [Get Strains By Search Term](actions/get-strains-by-search-term.md) | GET |  |

### Species Type Keys

| Action | Method | Description |
| --- | --- | --- |
| [Get Species Types](actions/get-species-types.md) | GET |  |

### Uniprot Mapping

| Action | Method | Description |
| --- | --- | --- |
| [Get UniProt Mapping](actions/get-uni-prot-mapping.md) | GET |  |

### Variant

| Action | Method | Description |
| --- | --- | --- |
| [Get Variant By RS ID](actions/get-variant-by-rs-id.md) | GET |  |
| [Get Variants By Position](actions/get-variants-by-position.md) | GET |  |


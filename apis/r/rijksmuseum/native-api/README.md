# Rijksmuseum: Native API Reference

A consolidated summary of Rijksmuseum's API configuration and 13 documented operations, with links to official documentation.

- **Official docs:** https://data.rijksmuseum.nl/docs
- **API base URL:** `https://data.rijksmuseum.nl`

## Authentication

### No Authentication

Rijksmuseum Data Services public APIs used by this app are available without tenant credentials or API keys.

This API does not require request authentication.

[Official authentication documentation](https://data.rijksmuseum.nl/docs)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `User-Agent` | `MindCloud Rijksmuseum App/1.0` |

Responses from this API use JSON. The next-page cursor is read from `next.id`.

## Filtering

Send filters in the query string.

## Retry behavior

Wait 500 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (13 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Dublin Core Object Metadata](actions/get-dublin-core-object-metadata.md) | `GET /{{metadataObjectId}}` | [docs](https://data.rijksmuseum.nl/docs/http/content-negotiation-arguments) |
| [Get IIIF Change Discovery Collection](actions/get-iiif-change-discovery-collection.md) | `GET /cd/collection.json` | [docs](https://data.rijksmuseum.nl/docs/iiif/cd) |
| [Get Latest IIIF Change Discovery Page](actions/get-latest-iiif-change-discovery-page.md) | `GET /cd/pages/last.json` | [docs](https://data.rijksmuseum.nl/docs/iiif/cd) |
| [Get LDES Collection](actions/get-ldes-collection.md) | `GET /ldes/collection.json` | [docs](https://data.rijksmuseum.nl/docs/ldes) |
| [Get Linked Art Object Metadata](actions/get-linked-art-object-metadata.md) | `GET /{{metadataObjectId}}` | [docs](https://data.rijksmuseum.nl/docs/http/content-negotiation-arguments) |
| [Get OAI Record](actions/get-oai-record.md) | `GET /oai` | [docs](https://data.rijksmuseum.nl/docs/oai-pmh/) |
| [Identify OAI PMH Repository](actions/identify-oai-pmh-repository.md) | `GET /oai` | [docs](https://data.rijksmuseum.nl/docs/oai-pmh/) |
| [List Metadata Representations](actions/list-metadata-representations.md) | `GET /{{metadataObjectId}}` | [docs](https://data.rijksmuseum.nl/docs/http/content-negotiation-arguments) |
| [List OAI Identifiers](actions/list-oai-identifiers.md) | `GET /oai` | [docs](https://data.rijksmuseum.nl/docs/oai-pmh/) |
| [List OAI Metadata Formats](actions/list-oai-metadata-formats.md) | `GET /oai` | [docs](https://data.rijksmuseum.nl/docs/oai-pmh/) |
| [List OAI Records](actions/list-oai-records.md) | `GET /oai` | [docs](https://data.rijksmuseum.nl/docs/oai-pmh/) |
| [List OAI Sets](actions/list-oai-sets.md) | `GET /oai` | [docs](https://data.rijksmuseum.nl/docs/oai-pmh/) |
| [Search Collection Objects](actions/search-collection-objects.md) | `GET /search/collection` | [docs](https://data.rijksmuseum.nl/docs/search) |

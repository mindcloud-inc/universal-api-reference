# <img src="https://images.mindcloud.co/apps/icons/rijksmuseum_1777486383639.png" alt="Rijksmuseum logo" width="28" height="28"> Rijksmuseum: Universal API

Access public Rijksmuseum Data Services for collection search, linked object metadata, OAI-PMH harvesting, LDES collection metadata, and IIIF Change Discovery feeds. The official public endpoints do not require authentication.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/rijksmuseum/latest
- **Category:** Productivity / Knowledge Management
- **Actions:** 13
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://data.rijksmuseum.nl/
- **Vendor API docs:** https://data.rijksmuseum.nl/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Dublin Core Object Metadata](actions/get-dublin-core-object-metadata.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rijksmuseum/latest/actions/get-dublin-core-object-metadata?connectionId=$CONNECTION_ID&metadataObjectId=200107928" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (13)

### Collection Object Metadata

| Action | Method | Description |
| --- | --- | --- |
| [Get Linked Art Object Metadata](actions/get-linked-art-object-metadata.md) | GET |  |

### Collection Object Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Search Collection Objects](actions/search-collection-objects.md) | GET |  |

### Dublin Core Metadata

| Action | Method | Description |
| --- | --- | --- |
| [Get Dublin Core Object Metadata](actions/get-dublin-core-object-metadata.md) | GET |  |

### Iiif Change Discovery Collection

| Action | Method | Description |
| --- | --- | --- |
| [Get IIIF Change Discovery Collection](actions/get-iiif-change-discovery-collection.md) | GET |  |

### Iiif Change Discovery Event

| Action | Method | Description |
| --- | --- | --- |
| [Get Latest IIIF Change Discovery Page](actions/get-latest-iiif-change-discovery-page.md) | GET |  |

### Ldes Collection

| Action | Method | Description |
| --- | --- | --- |
| [Get LDES Collection](actions/get-ldes-collection.md) | GET |  |

### Metadata Representation

| Action | Method | Description |
| --- | --- | --- |
| [List Metadata Representations](actions/list-metadata-representations.md) | GET |  |

### Oai Identifier

| Action | Method | Description |
| --- | --- | --- |
| [List OAI Identifiers](actions/list-oai-identifiers.md) | GET |  |

### Oai Metadata Format

| Action | Method | Description |
| --- | --- | --- |
| [List OAI Metadata Formats](actions/list-oai-metadata-formats.md) | GET |  |

### Oai Pmh Repository

| Action | Method | Description |
| --- | --- | --- |
| [Identify OAI PMH Repository](actions/identify-oai-pmh-repository.md) | GET |  |

### Oai Record

| Action | Method | Description |
| --- | --- | --- |
| [Get OAI Record](actions/get-oai-record.md) | GET |  |
| [List OAI Records](actions/list-oai-records.md) | GET |  |

### Oai Set

| Action | Method | Description |
| --- | --- | --- |
| [List OAI Sets](actions/list-oai-sets.md) | GET |  |


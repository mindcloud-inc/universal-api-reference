# Search for Synonyms with Algolia

Searches for synonyms in an Algolia index.

## Endpoint

- **Method:** `POST`
- **Path:** `/1/indexes/:indexName/synonyms/search`
- **Base URL:** `https://{applicationId}.algolia.net`
- **Official documentation:** [Search for Synonyms](https://www.algolia.com/doc/rest-api/search/search-synonyms)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `indexName` | path | `string` | yes | Name of the index on which to search synonyms. |
| `query` | body | `string` | no | Text query to search synonyms by object ID or terms. |
| `type` | body | `string` | no | Synonym type to filter by. |
| `page` | body | `number` | no | Results page number. |
| `hitsPerPage` | body | `number` | no | Maximum number of synonyms to return. |

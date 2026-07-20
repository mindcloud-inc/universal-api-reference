# Search for Facet Values with Algolia

Searches facet values in an Algolia index.

## Endpoint

- **Method:** `POST`
- **Path:** `/1/indexes/:indexName/facets/:facetName/query`
- **Base URL:** `https://{applicationId}.algolia.net`
- **Official documentation:** [Search for Facet Values](https://www.algolia.com/doc/rest-api/search/search-for-facet-values)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `indexName` | path | `string` | yes | The name of the Algolia index. |
| `facetName` | path | `string` | yes | The searchable facet attribute to query. |
| `facetQuery` | body | `string` | no | Text to search inside the facet values. |
| `maxFacetHits` | body | `number` | no | Maximum number of facet values to return. |
| `params` | body | `string` | no | URL-encoded search parameters to apply while searching facet values. |

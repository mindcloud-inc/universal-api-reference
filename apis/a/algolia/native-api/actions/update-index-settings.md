# Update Index Settings with Algolia

Updates existing index settings in Algolia.

## Endpoint

- **Method:** `PUT`
- **Path:** `/1/indexes/:indexName/settings`
- **Base URL:** `https://{applicationId}.algolia.net`
- **Official documentation:** [Update Index Settings](https://www.algolia.com/doc/rest-api/search/set-settings)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `indexName` | path | `string` | yes | The name of the Algolia index. |
| `attributesForFaceting[]` | body | `array<string>` | no | Facet configuration entries for the index. |
| `hitsPerPage` | body | `number` | no | Default number of hits per page. |
| `paginationLimitedTo` | body | `number` | no | Maximum number of hits available through pagination. |
| `forwardToReplicas` | query | `boolean` | no | Whether to apply the same settings to replica indices. |

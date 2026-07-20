# Delete an Index with Algolia

Deletes an existing index from Algolia.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/1/indexes/:indexName`
- **Base URL:** `https://{applicationId}.algolia.net`
- **Official documentation:** [Delete an Index](https://www.algolia.com/doc/rest-api/search/delete-index)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `indexName` | path | `string` | yes | The name of the Algolia index. |

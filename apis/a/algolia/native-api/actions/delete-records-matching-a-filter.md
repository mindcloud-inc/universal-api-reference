# Delete Records Matching a Filter with Algolia

Deletes records matching a filter in Algolia.

## Endpoint

- **Method:** `POST`
- **Path:** `/1/indexes/:indexName/deleteByQuery`
- **Base URL:** `https://{applicationId}.algolia.net`
- **Official documentation:** [Delete Records Matching a Filter](https://www.algolia.com/doc/rest-api/search/delete-by)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `indexName` | path | `string` | yes | The name of the Algolia index. |
| `filters` | body | `string` | yes | Filter expression that selects the records to delete. |

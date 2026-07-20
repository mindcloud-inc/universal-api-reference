# Delete a Record with Algolia

Deletes a record from an Algolia index.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/1/indexes/:indexName/:objectID`
- **Base URL:** `https://{applicationId}.algolia.net`
- **Official documentation:** [Delete a Record](https://www.algolia.com/doc/rest-api/search/delete-object)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `indexName` | path | `string` | yes | The name of the Algolia index. |
| `objectID` | path | `string` | yes | Unique identifier for the record to delete. |

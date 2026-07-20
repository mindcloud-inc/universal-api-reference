# Delete All Records from an Index with Algolia

Deletes all records from an Algolia index.

## Endpoint

- **Method:** `POST`
- **Path:** `/1/indexes/:indexName/clear`
- **Base URL:** `https://{applicationId}.algolia.net`
- **Official documentation:** [Delete All Records from an Index](https://www.algolia.com/doc/rest-api/search/clear-objects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `indexName` | path | `string` | yes | The name of the Algolia index. |

# Retrieve a Record with Algolia

Retrieves a record from an Algolia index.

## Endpoint

- **Method:** `GET`
- **Path:** `/1/indexes/:indexName/:objectID`
- **Base URL:** `https://{applicationId}.algolia.net`
- **Official documentation:** [Retrieve a Record](https://www.algolia.com/doc/rest-api/search/get-object)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `indexName` | path | `string` | yes | The name of the Algolia index. |
| `objectID` | path | `string` | yes | Unique identifier for the record. |

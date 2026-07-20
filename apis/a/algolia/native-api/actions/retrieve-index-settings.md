# Retrieve Index Settings with Algolia

Retrieves all index settings from Algolia.

## Endpoint

- **Method:** `GET`
- **Path:** `/1/indexes/:indexName/settings`
- **Base URL:** `https://{applicationId}.algolia.net`
- **Official documentation:** [Retrieve Index Settings](https://www.algolia.com/doc/rest-api/search/get-settings)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `indexName` | path | `string` | yes | The name of the Algolia index. |

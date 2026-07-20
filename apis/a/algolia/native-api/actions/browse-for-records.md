# Browse for Records with Algolia

Browses records in an Algolia index.

## Endpoint

- **Method:** `POST`
- **Path:** `/1/indexes/:indexName/browse`
- **Base URL:** `https://{applicationId}.algolia.net`
- **Official documentation:** [Browse for Records](https://www.algolia.com/doc/rest-api/search/browse)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `indexName` | path | `string` | yes | The name of the Algolia index to browse. |
| `params` | body | `string` | no | URL-encoded Algolia browse parameters. |

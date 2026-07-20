# List Documents with Xodo Sign

Retrieves documents from Xodo Sign.

## Endpoint

- **Method:** `GET`
- **Path:** `/document`
- **Base URL:** `https://api.eversign.com`
- **Official documentation:** [List Documents](https://eversign.com/api/documentation/methods#list-documents)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `business_id` | query | `string` | yes | The Xodo Sign business ID to query documents from. |
| `limit` | query | `string` | no | Maximum number of documents to return. |
| `page` | query | `string` | no | Page number to return. |

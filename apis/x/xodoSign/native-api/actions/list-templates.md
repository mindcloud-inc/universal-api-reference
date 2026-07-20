# List Templates with Xodo Sign

Retrieves templates from Xodo Sign.

## Endpoint

- **Method:** `GET`
- **Path:** `/document`
- **Base URL:** `https://api.eversign.com`
- **Official documentation:** [List Templates](https://eversign.com/api/documentation/methods#list-templates)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `business_id` | query | `string` | yes | The Xodo Sign business ID to query templates from. |
| `limit` | query | `string` | no | Maximum number of templates to return. |
| `page` | query | `string` | no | Page number to return. |

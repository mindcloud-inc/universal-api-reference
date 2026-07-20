# Delete Records with Mapsly

Deletes records from Mapsly.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/record`
- **Base URL:** `https://api.mapsly.com/v1`
- **Official documentation:** [Delete Records](https://developer.mapsly.com/docs/api/reference/REST-API.v1.yaml/paths/~1record/delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entity` | query | `string` | yes | The Mapsly entity API name to target, such as Leads. |
| `records[]` | body | `array<object>` | yes | Array of record objects to delete. |
| `callback_url` | query | `string` | no | Optional URL to receive async processing results. |
| `passthrough` | query | `string` | no | Optional value echoed back in callback payloads. |
| `async` | query | `boolean` | no | Queue the request instead of processing it synchronously. |

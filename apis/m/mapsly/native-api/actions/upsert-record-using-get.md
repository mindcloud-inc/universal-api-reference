# Upsert Record Using GET with Mapsly

Creates or updates a record in Mapsly using GET.

## Endpoint

- **Method:** `GET`
- **Path:** `/updaterecord`
- **Base URL:** `https://api.mapsly.com/v1`
- **Official documentation:** [Upsert Record Using GET](https://developer.mapsly.com/docs/api/reference/FORM-API.v1.yaml/paths/~1updaterecord/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entity` | query | `string` | yes | The Mapsly entity API name to target, such as Leads. |
| `id` | query | `string` | yes | The record identifier to insert or update. |
| `callback_url` | query | `string` | no | Optional URL to receive async processing results. |
| `passthrough` | query | `string` | no | Optional value echoed back in callback payloads. |
| `async` | query | `boolean` | no | Queue the request instead of processing it synchronously. |

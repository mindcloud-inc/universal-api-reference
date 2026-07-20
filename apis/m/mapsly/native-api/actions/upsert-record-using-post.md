# Upsert Record Using POST with Mapsly

Creates or updates a record in Mapsly using POST.

## Endpoint

- **Method:** `POST`
- **Path:** `/updaterecord`
- **Base URL:** `https://api.mapsly.com/v1`
- **Official documentation:** [Upsert Record Using POST](https://developer.mapsly.com/docs/api/reference/FORM-API.v1.yaml/paths/~1updaterecord/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entity` | query | `string` | yes | The Mapsly entity API name to target, such as Leads. |
| `id` | body | `string` | yes | The record identifier to insert or update. |
| `callback_url` | query | `string` | no | Optional URL to receive async processing results. |
| `passthrough` | query | `string` | no | Optional value echoed back in callback payloads. |
| `async` | query | `boolean` | no | Queue the request instead of processing it synchronously. |

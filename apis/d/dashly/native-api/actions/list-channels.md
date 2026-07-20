# List Channels with Dashly

Retrieves channels from a Dashly app.

## Endpoint

- **Method:** `GET`
- **Path:** `apps/:id/channels`
- **Base URL:** `https://api.dashly.app`
- **Official documentation:** [List Channels](https://developers.dashly.io/webapi/endpoints/apps/channels/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Dashly application ID. |
| `id_as_string` | query | `boolean` | no | Return IDs as strings. |

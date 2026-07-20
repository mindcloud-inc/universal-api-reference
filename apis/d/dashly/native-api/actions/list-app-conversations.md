# List App Conversations with Dashly

Retrieves conversations from a Dashly app.

## Endpoint

- **Method:** `GET`
- **Path:** `apps/:id/conversations`
- **Base URL:** `https://api.dashly.app`
- **Official documentation:** [List App Conversations](https://developers.dashly.io/webapi/endpoints/apps/conversations/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Dashly application ID. |
| `id_as_string` | query | `boolean` | no | Return IDs as strings. |

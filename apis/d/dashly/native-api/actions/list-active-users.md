# List Active Users with Dashly

Retrieves active users from a Dashly app.

## Endpoint

- **Method:** `GET`
- **Path:** `apps/:id/activeusers`
- **Base URL:** `https://api.dashly.app`
- **Official documentation:** [List Active Users](https://developers.dashly.io/webapi/endpoints/apps/activeusers/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Dashly application ID. |
| `id_as_string` | query | `boolean` | no | Return IDs as strings. |

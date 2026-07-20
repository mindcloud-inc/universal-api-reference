# List Webhooks with Smartcar

Retrieves webhook endpoints from Smartcar.

## Endpoint

- **Method:** `GET`
- **Path:** `https://management.api.smartcar.com/v3/webhooks`
- **Base URL:** `https://vehicle.api.smartcar.com/v3`
- **API:** rest
- **Official documentation:** [List Webhooks](https://smartcar.com/docs/api-reference/list-webhooks)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter[autoSubscribe]` | query | `boolean` | no | Filter webhooks by auto-subscribe setting. |
| `filter[callbackUri]` | query | `string` | no | Filter webhooks by callback URI. |
| `filter[isEnabled]` | query | `boolean` | no | Filter webhooks by enabled status. |
| `filter[name]` | query | `string` | no | Filter webhooks by display name. |

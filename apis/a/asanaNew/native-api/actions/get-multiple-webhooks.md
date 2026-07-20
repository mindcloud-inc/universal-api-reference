# Get multiple webhooks with Asana

Retrieves webhooks from Asana.

## Endpoint

- **Method:** `GET`
- **Path:** `webhooks`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Get multiple webhooks](https://developers.asana.com/reference/getwebhooks)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `opt_pretty` | query | `boolean` | no | Asana opt pretty parameter. |
| `limit` | query | `number` | no | Asana limit parameter. |
| `offset` | query | `string` | no | Asana offset parameter. |
| `workspace` | query | `string` | yes | Asana workspace parameter. |
| `resource` | query | `string` | no | Asana resource parameter. |
| `opt_fields` | query | `list<string>` | no | Asana opt fields parameter. |

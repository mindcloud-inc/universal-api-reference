# Get status updates from an object with Asana

Retrieves status updates for an object from Asana.

## Endpoint

- **Method:** `GET`
- **Path:** `status_updates`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Get status updates from an object](https://developers.asana.com/reference/getstatusesforobject)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `opt_pretty` | query | `boolean` | no | Asana opt pretty parameter. |
| `limit` | query | `number` | no | Asana limit parameter. |
| `offset` | query | `string` | no | Asana offset parameter. |
| `parent` | query | `string` | yes | Asana parent parameter. |
| `created_since` | query | `string` | no | Asana created since parameter. |
| `opt_fields` | query | `list<string>` | no | Asana opt fields parameter. |

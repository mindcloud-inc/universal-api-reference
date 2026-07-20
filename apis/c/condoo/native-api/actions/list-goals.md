# List Goals with condoo

Retrieves goals from condoo.

## Endpoint

- **Method:** `GET`
- **Path:** `/goals/`
- **Base URL:** `https://trk.condoo.systems/api`
- **Official documentation:** [List Goals](https://trk.condoo.systems/en/api-documentation/goals)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | no | Optional search string. |
| `search_by` | query | `string` | no | Optional search field. Allowed values: name, path, key. |
| `type` | query | `string` | no | Optional goal type. Allowed values: pageview, custom. |
| `website_id` | query | `number` | no | Optional website ID selector. |

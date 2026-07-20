# List Websites with condoo

Retrieves websites from condoo.

## Endpoint

- **Method:** `GET`
- **Path:** `/websites/`
- **Base URL:** `https://trk.condoo.systems/api`
- **Official documentation:** [List Websites](https://trk.condoo.systems/en/api-documentation/websites)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain_id` | query | `number` | no | Optional custom domain ID. |
| `is_enabled` | query | `boolean` | no | Optional enabled-state selector. |
| `search` | query | `string` | no | Optional search string. |
| `search_by` | query | `string` | no | Optional search field. Allowed value: domain. |
| `tracking_type` | query | `string` | no | Optional tracking type. Allowed values: normal, lightweight. |

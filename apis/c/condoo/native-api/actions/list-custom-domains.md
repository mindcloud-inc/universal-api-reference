# List Custom Domains with condoo

Retrieves custom domains from condoo.

## Endpoint

- **Method:** `GET`
- **Path:** `/domains/`
- **Base URL:** `https://trk.condoo.systems/api`
- **Official documentation:** [List Custom Domains](https://trk.condoo.systems/en/api-documentation/domains)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `is_enabled` | query | `boolean` | no | Optional enabled-state selector. |
| `search` | query | `string` | no | Optional search string. |
| `search_by` | query | `string` | no | Optional search field. Allowed value: host. |

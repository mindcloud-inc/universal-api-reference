# List Account Logs with condoo

Retrieves account logs from condoo.

## Endpoint

- **Method:** `GET`
- **Path:** `/logs/`
- **Base URL:** `https://trk.condoo.systems/api`
- **Official documentation:** [List Account Logs](https://trk.condoo.systems/en/api-documentation/users-logs)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `continent_code` | query | `string` | no | Optional continent code selector. |
| `country_code` | query | `string` | no | Optional country code selector. |
| `device_type` | query | `string` | no | Optional device type selector. |
| `search` | query | `string` | no | Optional search string. |
| `search_by` | query | `string` | no | Optional search field. Allowed value: city_name. |

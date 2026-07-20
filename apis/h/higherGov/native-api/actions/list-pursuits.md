# List Pursuits with HigherGov

Retrieves authenticated pursuits from HigherGov.

## Endpoint

- **Method:** `GET`
- **Path:** `/api-external/pursuit/`
- **Base URL:** `https://www.highergov.com`
- **Official documentation:** [List Pursuits](https://www.highergov.com/api-external/docs/#/api-external/api_external_pursuit_list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `reference_id` | query | `string` | no | Reference ID for the pursuit |
| `search_id` | query | `string` | no | HigherGov SearchID |
| `unique_key` | query | `string` | no | Unique internal pursuit key |

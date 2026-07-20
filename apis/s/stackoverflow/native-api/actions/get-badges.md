# Get Badges with Stackoverflow

Retrieves specific badges from Stackoverflow.

## Endpoint

- **Method:** `GET`
- **Path:** `/badges/[:ids]`
- **Base URL:** `https://api.stackexchange.com/2.3`
- **Official documentation:** [Get Badges](https://api.stackexchange.com/docs/badges-by-ids)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids` | path | `string` | yes | Semicolon-separated Stack Exchange badge IDs. |
| `site` | query | `string` | yes | Stack Exchange site parameter, for example stackoverflow. |

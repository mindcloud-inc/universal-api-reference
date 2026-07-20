# List German Districts by Federal State with OpenPLZ

## Endpoint

- **Method:** `GET`
- **Path:** `/de/FederalStates/{key}/Districts`
- **Base URL:** `https://openplzapi.org`
- **Official documentation:** [List German Districts by Federal State](https://www.openplzapi.org/en/germany/#requesting-districts)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `key` | path | `string` | yes | German federal state key, such as 09 for Bavaria. |

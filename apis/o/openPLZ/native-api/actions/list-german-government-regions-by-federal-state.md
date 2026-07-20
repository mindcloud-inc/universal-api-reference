# List German Government Regions by Federal State with OpenPLZ

## Endpoint

- **Method:** `GET`
- **Path:** `/de/FederalStates/{key}/GovernmentRegions`
- **Base URL:** `https://openplzapi.org`
- **Official documentation:** [List German Government Regions by Federal State](https://www.openplzapi.org/en/germany/#requesting-government-regions)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `key` | path | `string` | yes | German federal state key, such as 09 for Bavaria. |

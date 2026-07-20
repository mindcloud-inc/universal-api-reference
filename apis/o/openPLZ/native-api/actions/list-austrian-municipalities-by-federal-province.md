# List Austrian Municipalities by Federal Province with OpenPLZ

## Endpoint

- **Method:** `GET`
- **Path:** `/at/FederalProvinces/{key}/Municipalities`
- **Base URL:** `https://openplzapi.org`
- **Official documentation:** [List Austrian Municipalities by Federal Province](https://www.openplzapi.org/en/austria/#requesting-municipalities)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `key` | path | `string` | yes | Austrian federal province key. |

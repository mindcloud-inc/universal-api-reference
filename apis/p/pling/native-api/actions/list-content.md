# List Content with Pling

Retrieves public content listings from Pling.

## Endpoint

- **Method:** `GET`
- **Path:** `/content/data`
- **Base URL:** `https://api.pling.com/ocs/v1`
- **Official documentation:** [List Content](https://www.opendesktop.org/ocs-api)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sortmode` | query | `string` | no | Pling sort mode such as new or high. Accepted values: `0`, `1`, `2`, `3`. |

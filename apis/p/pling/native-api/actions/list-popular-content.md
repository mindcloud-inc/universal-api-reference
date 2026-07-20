# List Popular Content with Pling

Retrieves popular public content from Pling.

## Endpoint

- **Method:** `GET`
- **Path:** `/content/data`
- **Base URL:** `https://api.pling.com/ocs/v1`
- **Official documentation:** [List Popular Content](https://www.opendesktop.org/ocs-api)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sortmode` | query | `string` | no | Pling sort mode. The default high lists popular content. Accepted values: `0`, `1`, `2`, `3`. |

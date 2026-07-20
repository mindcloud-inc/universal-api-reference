# Search Content with Pling

Finds public content in Pling by search text.

## Endpoint

- **Method:** `GET`
- **Path:** `/content/data`
- **Base URL:** `https://api.pling.com/ocs/v1`
- **Official documentation:** [Search Content](https://www.opendesktop.org/ocs-api)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | yes | Text to search for in public Pling content. |

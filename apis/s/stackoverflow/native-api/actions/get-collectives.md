# Get Collectives with Stackoverflow

Retrieves specific collectives from Stackoverflow.

## Endpoint

- **Method:** `GET`
- **Path:** `/collectives/[:slugs]`
- **Base URL:** `https://api.stackexchange.com/2.3`
- **Official documentation:** [Get Collectives](https://api.stackexchange.com/docs/collectives-by-slug)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `slugs` | path | `string` | yes | Semicolon-delimited collective slugs. |

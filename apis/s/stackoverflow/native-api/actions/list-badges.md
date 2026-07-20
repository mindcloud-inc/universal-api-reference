# List Badges with Stackoverflow

Retrieves badges from Stackoverflow.

## Endpoint

- **Method:** `GET`
- **Path:** `/badges`
- **Base URL:** `https://api.stackexchange.com/2.3`
- **Official documentation:** [List Badges](https://api.stackexchange.com/docs/badges)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `site` | query | `string` | yes | Stack Exchange site parameter, for example stackoverflow. |

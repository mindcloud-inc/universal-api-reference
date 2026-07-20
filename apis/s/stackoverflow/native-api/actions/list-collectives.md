# List Collectives with Stackoverflow

Retrieves collectives from Stackoverflow.

## Endpoint

- **Method:** `GET`
- **Path:** `/collectives`
- **Base URL:** `https://api.stackexchange.com/2.3`
- **Official documentation:** [List Collectives](https://api.stackexchange.com/docs/collectives)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `site` | query | `string` | yes | API site parameter, for example stackoverflow. |

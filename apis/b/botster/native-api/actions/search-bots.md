# Search Bots with Botster

Finds bots in Botster by search query.

## Endpoint

- **Method:** `GET`
- **Path:** `/bots`
- **Base URL:** `https://botster.io/api/v2`
- **Official documentation:** [Search Bots](https://botster.io/info/api-docs)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | no | Search query used to filter the Botster bot catalog. |

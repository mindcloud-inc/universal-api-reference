# Get Comments with Stackoverflow

Retrieves specific comments from Stackoverflow.

## Endpoint

- **Method:** `GET`
- **Path:** `/comments/[:ids]`
- **Base URL:** `https://api.stackexchange.com/2.3`
- **Official documentation:** [Get Comments](https://api.stackexchange.com/docs/comments-by-ids)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids` | path | `string` | yes | Semicolon-separated Stack Exchange comment IDs. |
| `site` | query | `string` | yes | Stack Exchange site parameter, for example stackoverflow. |

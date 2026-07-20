# List Comments with Stackoverflow

Retrieves comments from Stackoverflow.

## Endpoint

- **Method:** `GET`
- **Path:** `/comments`
- **Base URL:** `https://api.stackexchange.com/2.3`
- **Official documentation:** [List Comments](https://api.stackexchange.com/docs/comments)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `site` | query | `string` | yes | Stack Exchange site parameter, for example stackoverflow. |

# List Tags with Stackoverflow

Retrieves tags from Stackoverflow.

## Endpoint

- **Method:** `GET`
- **Path:** `/tags`
- **Base URL:** `https://api.stackexchange.com/2.3`
- **Official documentation:** [List Tags](https://api.stackexchange.com/docs/tags)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `site` | query | `string` | yes | Stack Exchange site parameter, for example stackoverflow. |

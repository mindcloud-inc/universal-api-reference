# Get Tag Info with Stackoverflow

Retrieves specific tag information from Stackoverflow.

## Endpoint

- **Method:** `GET`
- **Path:** `/tags/[:tags]/info`
- **Base URL:** `https://api.stackexchange.com/2.3`
- **Official documentation:** [Get Tag Info](https://api.stackexchange.com/docs/tags-by-name)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tags` | path | `string` | yes | Semicolon-delimited tag names. |
| `site` | query | `string` | yes | API site parameter, for example stackoverflow. |

# List Posts with Stackoverflow

Retrieves posts from Stackoverflow.

## Endpoint

- **Method:** `GET`
- **Path:** `/posts`
- **Base URL:** `https://api.stackexchange.com/2.3`
- **Official documentation:** [List Posts](https://api.stackexchange.com/docs/posts)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `site` | query | `string` | yes | Stack Exchange site parameter, for example stackoverflow. |

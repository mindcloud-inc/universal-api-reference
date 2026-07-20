# List Related Tags with Stackoverflow

Retrieves related tags from Stackoverflow.

## Endpoint

- **Method:** `GET`
- **Path:** `/tags/[:tags]/related`
- **Base URL:** `https://api.stackexchange.com/2.3`
- **Official documentation:** [List Related Tags](https://api.stackexchange.com/docs/related-tags)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tags` | path | `string` | yes | Semicolon-delimited tag names. |
| `site` | query | `string` | yes | API site parameter, for example stackoverflow. |

# List Tag Synonyms with Stackoverflow

Retrieves tag synonyms for specific tags from Stackoverflow.

## Endpoint

- **Method:** `GET`
- **Path:** `/tags/[:tags]/synonyms`
- **Base URL:** `https://api.stackexchange.com/2.3`
- **Official documentation:** [List Tag Synonyms](https://api.stackexchange.com/docs/synonyms-by-tags)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tags` | path | `string` | yes | Semicolon-delimited tag names. |
| `site` | query | `string` | yes | API site parameter, for example stackoverflow. |

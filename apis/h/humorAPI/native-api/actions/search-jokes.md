# Search Jokes with Humor API

## Endpoint

- **Method:** `GET`
- **Path:** `/jokes/search`
- **Base URL:** `https://api.humorapi.com`
- **Official documentation:** [Search Jokes](https://humorapi.com/docs/#Search-Jokes)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `keywords` | query | `string` | no | Comma-separated words that must occur in the joke. |
| `include-tags` | query | `string` | no | Comma-separated tags the jokes should include. |
| `exclude-tags` | query | `string` | no | Comma-separated tags the jokes must not include. |
| `min-rating` | query | `number` | no | Minimum joke rating between 0 and 10. |
| `max-length` | query | `number` | no | Maximum joke length in letters. |

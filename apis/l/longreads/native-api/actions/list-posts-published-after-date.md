# List Posts Published After Date with Longreads

Retrieves Longreads posts published after a date.

## Endpoint

- **Method:** `GET`
- **Path:** `/wp/v2/posts`
- **Base URL:** `https://longreads.com/wp-json`
- **Official documentation:** [List Posts Published After Date](https://longreads.com/wp-json/wp/v2/posts)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `after` | query | `date` | yes | Return posts published after this ISO 8601 datetime. |

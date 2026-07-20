# List Links by Original URL with Short.io

Finds links in Short.io by original URL.

## Endpoint

- **Method:** `GET`
- **Path:** `/links/multiple-by-url`
- **Base URL:** `https://api.short.io`
- **Official documentation:** [List Links by Original URL](https://developers.short.io/reference/get_links-multiple-by-url)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | query | `string` | yes | Domain hostname. |
| `originalURL` | query | `string` | yes | Link original URL. |

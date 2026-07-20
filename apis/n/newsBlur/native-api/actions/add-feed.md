# Add Feed with NewsBlur

Adds a feed to NewsBlur.

## Endpoint

- **Method:** `POST`
- **Path:** `/reader/add_url`
- **Base URL:** `https://www.newsblur.com`
- **Official documentation:** [Add Feed](https://newsblur.com/api)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | RSS feed URL or website URL to add. |
| `folder` | body | `string` | no | Folder to place the feed in. Omit for top level. |

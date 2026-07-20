# List Favicons with NewsBlur

Retrieves feed favicons from NewsBlur.

## Endpoint

- **Method:** `GET`
- **Path:** `/reader/favicons`
- **Base URL:** `https://www.newsblur.com`
- **Official documentation:** [List Favicons](https://newsblur.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `feed_ids` | query | `number<number>` | no | Feed ID to retrieve a favicon for. NewsBlur supports repeating feed_ids for multiple feeds. |

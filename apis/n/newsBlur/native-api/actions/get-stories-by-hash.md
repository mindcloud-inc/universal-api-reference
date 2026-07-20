# Get Stories By Hash with NewsBlur

Retrieves stories from NewsBlur by story hash.

## Endpoint

- **Method:** `GET`
- **Path:** `/reader/river_stories`
- **Base URL:** `https://www.newsblur.com`
- **Official documentation:** [Get Stories By Hash](https://newsblur.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `h` | query | `string` | yes | Story hash to retrieve. NewsBlur supports repeating h up to 100 hashes. |

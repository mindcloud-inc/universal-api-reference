# List Starred Stories with NewsBlur

Retrieves starred stories from NewsBlur.

## Endpoint

- **Method:** `GET`
- **Path:** `/reader/starred_stories`
- **Base URL:** `https://www.newsblur.com`
- **Official documentation:** [List Starred Stories](https://newsblur.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `h` | query | `string<string>` | no | Story hash to load from saved stories. NewsBlur supports repeating h up to 100 hashes. |
| `tag` | query | `string` | no | Only load saved stories under a specific tag. |
| `highlights` | query | `boolean` | no | Only load stories that have highlighting. |
| `query` | query | `string` | no | Search keyword or phrase in saved stories. NewsBlur notes feed search is premium-only. |

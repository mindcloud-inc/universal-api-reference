# Autocomplete Feeds with NewsBlur

Finds feeds in NewsBlur by search phrase.

## Endpoint

- **Method:** `GET`
- **Path:** `/rss_feeds/feed_autocomplete`
- **Base URL:** `https://www.newsblur.com`
- **Official documentation:** [Autocomplete Feeds](https://newsblur.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `term` | query | `string` | yes | Phrase to search for in feed address, URL, and title. |

# Website to RSS Feed with World News API

Converts a website to an RSS feed using World News API.

## Endpoint

- **Method:** `GET`
- **Path:** `/feed.rss`
- **Base URL:** `https://api.worldnewsapi.com`
- **Official documentation:** [Website to RSS Feed](https://worldnewsapi.com/docs/website-to-rss-feed/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `extract-news` | query | `boolean` | no | When true, extract full news details into the RSS output. |
| `url` | query | `string` | yes | Website URL to convert into an RSS feed. |

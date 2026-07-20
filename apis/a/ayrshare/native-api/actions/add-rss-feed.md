# Add RSS Feed with Ayrshare

Creates a new RSS feed in Ayrshare.

## Endpoint

- **Method:** `POST`
- **Path:** `/feed`
- **Base URL:** `https://api.ayrshare.com/api`
- **Official documentation:** [Add RSS Feed](https://www.ayrshare.com/docs/apis/feeds/add-feed)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | RSS feed URL to add for automated posting. |
| `platforms[]` | body | `array<string>` | yes | Platforms the feed should publish to when new items are found. |

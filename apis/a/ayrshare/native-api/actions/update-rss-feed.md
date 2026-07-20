# Update RSS Feed with Ayrshare

Updates an existing RSS feed in Ayrshare.

## Endpoint

- **Method:** `PUT`
- **Path:** `/feed`
- **Base URL:** `https://api.ayrshare.com/api`
- **Official documentation:** [Update RSS Feed](https://www.ayrshare.com/docs/apis/feeds/update-feed)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | Ayrshare RSS feed ID to update. |
| `url` | body | `string` | no | Updated RSS feed URL. |

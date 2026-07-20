# Search Hashtags with Ayrshare

Searches hashtag posts in Ayrshare.

## Endpoint

- **Method:** `GET`
- **Path:** `/hashtags/search`
- **Base URL:** `https://api.ayrshare.com/api`
- **Official documentation:** [Search Hashtags](https://www.ayrshare.com/docs/apis/hashtags/search-hashtags)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `keyword` | query | `string` | yes | Hashtag keyword to search for public Instagram media. |
| `searchType` | query | `string` | no | Search type such as top or recent, when supported by Ayrshare. Accepted values: `recent`, `top`. |

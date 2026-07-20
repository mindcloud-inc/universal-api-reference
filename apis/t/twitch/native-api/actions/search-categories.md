# Search Categories with Twitch

Searches Twitch categories using a query.

## Endpoint

- **Method:** `GET`
- **Path:** `/search/categories`
- **Base URL:** `https://api.twitch.tv/helix`
- **Official documentation:** [Search Categories](https://dev.twitch.tv/docs/api/reference#search-categories)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | yes | The URI-encoded search string. |
| `first` | query | `number` | no | The maximum number of objects to return. Maximum: 100. Default: 20. |
| `after` | query | `string` | no | The cursor used to get the next page of results. |

# Search Articles with GNews

Searches GNews for news articles by keyword.

## Endpoint

- **Method:** `GET`
- **Path:** `/search`
- **Base URL:** `https://gnews.io/api/v4`
- **Official documentation:** [Search Articles](https://docs.gnews.io/endpoints/search-endpoint)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | yes | Keywords used to find matching news articles. |
| `lang` | query | `string` | no | Filter returned articles by language code. |
| `country` | query | `string` | no | Filter returned articles by publication country code. |
| `max` | query | `number` | no | Maximum number of articles to return per page. |
| `in` | query | `string` | no | Choose which article fields are searched for the query terms. |
| `nullable` | query | `string` | no | Allow selected attributes to be returned as null. |
| `from` | query | `date` | no | Only include articles published on or after this ISO 8601 timestamp. |
| `to` | query | `date` | no | Only include articles published on or before this ISO 8601 timestamp. |
| `sortby` | query | `string` | no | Sort articles by publication date or relevance. |
| `page` | query | `number` | no | Page number to return. |
| `truncate` | query | `string` | no | Truncate selected fields such as content. |

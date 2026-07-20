# Search Everything with News API

Finds articles in News API by keyword or phrase.

## Endpoint

- **Method:** `GET`
- **Path:** `/everything`
- **Base URL:** `https://newsapi.org/v2`
- **Official documentation:** [Search Everything](https://newsapi.org/docs/endpoints/everything)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domains` | query | `string` | no | Comma-separated domains to include. |
| `excludeDomains` | query | `string` | no | Comma-separated domains to exclude. |
| `from` | query | `string` | no | A date and optional time for the oldest allowed article. |
| `q` | query | `string` | no | Keywords or a phrase to search for. |
| `searchIn` | query | `string` | no | Restrict the search to article fields such as title, description, or content. |
| `sources` | query | `string` | no | Comma-separated source identifiers to search within. |
| `to` | query | `string` | no | A date and optional time for the newest allowed article. |
| `language` | query | `string` | no | Restrict articles to a single language. Accepted values: `0`, `1`, `10`, `11`, `12`, `2`, `3`, `4`, `5`, `6`, `7`, `8`, `9`. |
| `sortBy` | query | `string` | no | Sort order for returned articles. Accepted values: `0`, `1`, `2`. |
| `pageSize` | query | `number` | no | Number of results to return per page. |
| `page` | query | `number` | no | Page number of the results to return. |

# Search News with World News API

Finds news articles in World News API by filter criteria.

## Endpoint

- **Method:** `GET`
- **Path:** `/search-news`
- **Base URL:** `https://api.worldnewsapi.com`
- **Official documentation:** [Search News](https://worldnewsapi.com/docs/search-news/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `authors` | query | `string` | no | Comma-separated list of author names to include. Send multiple values as a string separated by `,`. |
| `categories` | query | `string` | no | Comma-separated list of news categories to include. Send multiple values as a string separated by `,`. |
| `earliest-publish-date` | query | `date` | no | Earliest publish date/time to include. |
| `entities` | query | `string` | no | Comma-separated list of named entities to match. Send multiple values as a string separated by `,`. |
| `language` | query | `string` | no | Two-letter language code to restrict article language. |
| `latest-publish-date` | query | `date` | no | Latest publish date/time to include. |
| `location-filter` | query | `string` | no | Location filter expression for nearby or regional news. |
| `max-sentiment` | query | `number` | no | Maximum sentiment score for returned articles. |
| `min-sentiment` | query | `number` | no | Minimum sentiment score for returned articles. |
| `news-sources` | query | `string` | no | Comma-separated list of source names to include. Send multiple values as a string separated by `,`. |
| `number` | query | `number` | no | Maximum number of articles to return. |
| `offset` | query | `number` | no | Zero-based offset for paginating through search results. |
| `sort` | query | `string` | no | Field to sort the results by. |
| `sort-direction` | query | `string` | no | Sort direction for the selected sort field. |
| `source-country` | query | `string` | no | Two-letter country code to restrict article sources. |
| `text` | query | `string` | no | Free-text query to search for matching news articles. |
| `text-match-indexes` | query | `boolean` | no | Return match index metadata for the searched text. |

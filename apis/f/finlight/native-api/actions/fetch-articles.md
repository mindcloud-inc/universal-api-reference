# Fetch Articles with finlight

Finds financial news articles in finlight.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/articles`
- **Base URL:** `https://api.finlight.me`
- **Official documentation:** [Fetch Articles](https://docs.finlight.me/v2/rest-endpoints/#fetch-articles)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | no | Search query with optional advanced field filters. |
| `tickers[]` | body | `array<string>` | no | Filter articles by stock ticker symbols. |
| `sources[]` | body | `array<string>` | no | Filter articles by source domain list. |
| `excludeSources[]` | body | `array<string>` | no | Exclude source domains from the results. |
| `countries[]` | body | `array<string>` | no | Filter articles by ISO 3166-1 alpha-2 country codes. |
| `language` | body | `string` | no | Filter results by ISO 639-1 language code. |
| `from` | body | `string` | no | Start date in YYYY-MM-DD format or ISO datetime. |
| `to` | body | `string` | no | End date in YYYY-MM-DD format or ISO datetime. |
| `includeEntities` | body | `boolean` | no | Include company entities when the subscription tier supports them. |
| `orderBy` | body | `string` | no | Sort field: publishDate or createdAt. |
| `order` | body | `string` | no | Sort direction: ASC or DESC. |
| `pageSize` | body | `number` | no | Number of results per page. |
| `page` | body | `number` | no | Page number. |

# Enrich News with Zoominfo

Enriches company news with ZoomInfo data.

## Endpoint

- **Method:** `POST`
- **Path:** `enrich/news`
- **Base URL:** `https://api.zoominfo.com/`
- **Official documentation:** [Enrich News](https://api-docs.zoominfo.com/#a04f60d9-353e-4eb1-9c37-0539ee6b8d13)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyId` | body | `number` | no | The id of the company you are searching for |
| `limit` | body | `number` | no | Number of articles to return per page, the maximum limit is 100. |
| `page` | body | `number` | no | Provides the results for the given page, used in conjunction with limit. |
| `categories[]` | body | `array<string>` | no | Category of news articles. Accepts an Array of String. See the 'News Categories' endpoint for values. |
| `url[]` | body | `array<string>` | no | Search news by URL strings. Accepts an Array of String. Minimum of 5 characters per input |
| `pageDateMin` | body | `string` | no | Specify the earliest publishing date for news articles returned. For example, 2020-01-01 will return all news articles published on or after Jan 1, 2020. |
| `pageDateMax` | body | `string` | no | Specify the latest publishing date for news articles articles. For example, 2020-01-31 will return all new articles published on or before Jan 31, 2020. |

# List News with Zoominfo

Finds news in ZoomInfo by search criteria.

## Endpoint

- **Method:** `POST`
- **Path:** `search/news`
- **Base URL:** `https://api.zoominfo.com/`
- **Official documentation:** [List News](https://api-docs.zoominfo.com/#4c4c979b-4495-4a17-8925-7d00c52c7e19)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `categories[]` | body | `array<string>` | no | Category of news articles. Accepts an Array of String. See the 'News Categories' endpoint for values. |
| `url[]` | body | `array<string>` | no | Search news by URL strings. Accepts an Array of String. Minimum of 5 characters per input |
| `pageDateMin` | body | `string` | no | Specify the earliest publishing date for news articles returned. For example, 2020-01-01 will return all news articles published on or after Jan 1, 2020. |
| `pageDateMax` | body | `string` | no | Specify the latest publishing date for news articles articles. For example, 2020-01-31 will return all new articles published on or before Jan 31, 2020. |

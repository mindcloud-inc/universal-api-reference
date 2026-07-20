# List Top Headlines with GNews

Retrieves current top news headlines from GNews.

## Endpoint

- **Method:** `GET`
- **Path:** `/top-headlines`
- **Base URL:** `https://gnews.io/api/v4`
- **Official documentation:** [List Top Headlines](https://docs.gnews.io/endpoints/top-headlines-endpoint)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | no | Keywords used to find relevant headlines. |
| `category` | query | `string` | no | Filter headlines by category. |
| `lang` | query | `string` | no | Filter headlines by article language code. |
| `country` | query | `string` | no | Filter headlines by country code. |
| `max` | query | `number` | no | Maximum number of articles to return. |
| `page` | query | `number` | no | Page number to return. |
| `from` | query | `date` | no | Only include articles published on or after this date and time. |
| `to` | query | `date` | no | Only include articles published on or before this date and time. |
| `nullable` | query | `string` | no | Fields allowed to return null values. |
| `truncate` | query | `string` | no | Truncate the content field when set to content. |

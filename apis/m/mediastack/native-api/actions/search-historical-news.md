# Search Historical News with Mediastack

Finds historical news articles in Mediastack.

## Endpoint

- **Method:** `GET`
- **Path:** `/news`
- **Base URL:** `https://api.mediastack.com/v1`
- **Official documentation:** [Search Historical News](https://mediastack.com/documentation)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date` | query | `string` | yes | Required historical date or date range, such as 2026-04-30 or 2026-04-01,2026-04-30. |
| `keywords` | query | `string` | no | One or more comma-separated search keywords. Prefix a keyword with - to exclude it. |
| `sources` | query | `string` | no | One or more comma-separated source codes, such as abc-news. Prefix a source code with - to exclude it. |
| `categories` | query | `string` | no | One or more comma-separated categories. Prefix a category with - to exclude it. |
| `countries` | query | `string` | no | One or more comma-separated 2-letter country codes. Prefix a country with - to exclude it. |
| `languages` | query | `string` | no | One or more comma-separated 2-letter language codes. Prefix a language with - to exclude it. |

# Search News Sources with Mediastack

Finds news sources in Mediastack.

## Endpoint

- **Method:** `GET`
- **Path:** `/sources`
- **Base URL:** `https://api.mediastack.com/v1`
- **Official documentation:** [Search News Sources](https://mediastack.com/documentation)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | yes | Required search keyword for matching news sources. |
| `countries` | query | `string` | no | One or more comma-separated 2-letter country codes. Prefix a country with - to exclude it. |
| `languages` | query | `string` | no | One or more comma-separated 2-letter language codes. Prefix a language with - to exclude it. |
| `categories` | query | `string` | no | One or more comma-separated categories. Prefix a category with - to exclude it. |

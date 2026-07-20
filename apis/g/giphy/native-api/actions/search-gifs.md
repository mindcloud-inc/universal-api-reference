# Search GIFs with Giphy

Finds GIFs in Giphy by search phrase.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/gifs/search`
- **Base URL:** `https://api.giphy.com/`
- **Official documentation:** [Search GIFs](https://developers.giphy.com/docs/api/endpoint/#search)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | yes | Search phrase exactly as the user entered it. |
| `lang` | query | `string` | no | ISO-639-1 language code for the search phrase. |
| `rating` | query | `string` | no | Maximum content rating to return. |
| `random_id` | query | `string` | no | Session-level random ID from the Random ID endpoint. |
| `bundle` | query | `string` | no | Rendition bundle to limit returned image variants. |
| `country_code` | query | `string` | no | ISO-3166-1 alpha-2 country code for proxied requests. |
| `region` | query | `string` | no | ISO-3166-2 subdivision code for proxied requests. |
| `remove_low_contrast` | query | `boolean` | no | Exclude low-contrast results when true. |

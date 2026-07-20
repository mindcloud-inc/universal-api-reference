# Search Google with SerpApi

Retrieves Google search results from SerpApi.

## Endpoint

- **Method:** `GET`
- **Path:** `/search.json`
- **Base URL:** `https://serpapi.com`
- **Official documentation:** [Search Google](https://serpapi.com/search-api)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | yes | The Google search query to run through SerpApi. |
| `location` | query | `string` | no | Search origin location, ideally at city level. |
| `google_domain` | query | `string` | no | Google domain to use, such as google.com. |
| `gl` | query | `string` | no | Two-letter country code for Google country targeting. |
| `hl` | query | `string` | no | Two-letter Google interface language code. |
| `no_cache` | query | `boolean` | no | Set true to force a fresh SerpApi request instead of reusing cache. |

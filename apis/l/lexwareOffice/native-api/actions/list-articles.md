# List Articles with Lexware Office

Retrieves a list of articles from Lexware Office.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/articles`
- **Base URL:** `https://api.lexware.io`
- **Official documentation:** [List Articles](https://developers.lexware.io/docs/#articles-endpoint-filtering-articles)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `articleNumber` | query | `string` | no | Filter articles by article number. |
| `gtin` | query | `string` | no | Filter articles by GTIN. |
| `type` | query | `string` | no | Filter articles by type. |

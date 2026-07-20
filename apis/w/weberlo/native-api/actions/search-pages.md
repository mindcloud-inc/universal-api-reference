# Search Pages with Weberlo

Finds pages in Weberlo by search query.

## Endpoint

- **Method:** `GET`
- **Path:** `/page/search`
- **Base URL:** `https://connect.weberlo.com`
- **Official documentation:** [Search Pages](https://developers.weberlo.com/#tag/Page/paths/~1page~1search/get)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | yes | Search term for matching pages. |

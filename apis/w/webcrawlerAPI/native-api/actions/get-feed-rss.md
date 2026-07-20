# Get Feed RSS with Webcrawler API

Retrieves feed changes in Atom format from Webcrawler API.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/feed/:id/rss`
- **Base URL:** `https://api.webcrawlerapi.com`
- **Official documentation:** [Get Feed RSS](https://webcrawlerapi.com/docs/api/feed/feed-rss)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Feed identifier returned by List Feeds. |

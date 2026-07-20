# Get Feed JSON with Webcrawler API

Retrieves feed changes in JSON Feed format from Webcrawler API.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/feed/:id/json`
- **Base URL:** `https://api.webcrawlerapi.com`
- **Official documentation:** [Get Feed JSON](https://webcrawlerapi.com/docs/api/feed/feed-json)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Feed identifier returned by List Feeds. |

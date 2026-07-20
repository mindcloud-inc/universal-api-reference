# List Subscriptions with YouTube

Retrieves one or more subscriptions from YouTube.

## Endpoint

- **Method:** `GET`
- **Path:** `/youtube/v3/subscriptions`
- **Base URL:** `https://www.googleapis.com`
- **Official documentation:** [List Subscriptions](https://developers.google.com/youtube/v3/docs/subscriptions/list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `part` | query | `string` | yes | Comma-separated subscription resource parts to include. |
| `channelId` | query | `string` | no | Filter subscriptions by channel ID. |
| `id` | query | `string` | no | Comma-separated list of subscription IDs. |
| `myRecentSubscribers` | query | `boolean` | no | Return recent subscribers for the authenticated channel. |
| `mySubscribers` | query | `boolean` | no | Return subscribers for the authenticated channel. |

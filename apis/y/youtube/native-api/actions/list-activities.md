# List Activities with YouTube

Retrieves channel activity items from YouTube.

## Endpoint

- **Method:** `GET`
- **Path:** `/youtube/v3/activities`
- **Base URL:** `https://www.googleapis.com`
- **Official documentation:** [List Activities](https://developers.google.com/youtube/v3/docs/activities/list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `part` | query | `string` | yes | Comma-separated activity resource parts to include. |
| `channelId` | query | `string` | no | Return activities for a specific channel. |
| `home` | query | `boolean` | no | Retrieve feed activities from subscriptions. |
| `publishedAfter` | query | `date` | no | Return activities published after this timestamp. |
| `publishedBefore` | query | `date` | no | Return activities published before this timestamp. |
| `regionCode` | query | `string` | no | Region code for regional filtering. |

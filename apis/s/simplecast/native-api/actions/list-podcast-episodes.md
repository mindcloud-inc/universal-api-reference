# List Podcast Episodes with Simplecast

Retrieves episodes for a podcast from Simplecast.

## Endpoint

- **Method:** `GET`
- **Path:** `/podcasts/:podcast_id/episodes`
- **Base URL:** `https://api.simplecast.com`
- **Official documentation:** [List Podcast Episodes](https://apidocs.simplecast.com/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `podcast_id` | path | `string` | yes | Simplecast podcast identifier. |

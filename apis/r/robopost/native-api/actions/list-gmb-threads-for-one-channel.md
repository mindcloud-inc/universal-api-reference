# List GMB Threads for One Channel with Robopost

Retrieves Google Business threads for one Robopost channel.

## Endpoint

- **Method:** `GET`
- **Path:** `/social_inbox_items/channels/{channel_id}/gmb/threads`
- **Base URL:** `https://public-api.robopost.app/v1`
- **Official documentation:** [List GMB Threads for One Channel](https://robopost.app/docs/robopost-api/)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channel_id` | path | `string` | yes | The Robopost channel ID. This endpoint only works for Google Business channels. |

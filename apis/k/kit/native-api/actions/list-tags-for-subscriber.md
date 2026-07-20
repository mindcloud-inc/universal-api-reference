# List Tags for Subscriber with Kit

Lists tags for a Kit subscriber.

## Endpoint

- **Method:** `GET`
- **Path:** `/subscribers/:subscriber_id/tags`
- **Base URL:** `https://api.kit.com/v4`
- **Official documentation:** [List Tags for Subscriber](https://developers.kit.com/api-reference/subscribers/list-tags-for-a-subscriber)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subscriber_id` | path | `number` | yes | Kit subscriber ID whose tags should be listed. |
| `include_total_count` | query | `boolean` | no | Set to true to include total_count in the response. Kit notes this can make the request slower. |

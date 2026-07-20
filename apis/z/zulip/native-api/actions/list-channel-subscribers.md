# List Channel Subscribers with Zulip

Retrieves subscribers for a specific Zulip channel.

## Endpoint

- **Method:** `GET`
- **Path:** `/streams/:stream_id/members`
- **Base URL:** `{site}/api/v1`
- **Official documentation:** [List Channel Subscribers](https://zulip.com/api/get-subscribers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `stream_id` | path | `number` | yes | The target channel ID. |

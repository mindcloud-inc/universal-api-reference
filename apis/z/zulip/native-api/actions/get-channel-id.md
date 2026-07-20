# Get Channel ID with Zulip

Finds a Zulip channel ID by name.

## Endpoint

- **Method:** `GET`
- **Path:** `/get_stream_id`
- **Base URL:** `{site}/api/v1`
- **Official documentation:** [Get Channel ID](https://zulip.com/api/get-stream-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `stream` | query | `string` | yes | The name of the channel to access. |

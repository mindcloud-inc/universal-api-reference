# List Topics in a Channel with Zulip

Retrieves topics in a specific Zulip channel.

## Endpoint

- **Method:** `GET`
- **Path:** `/users/me/:stream_id/topics`
- **Base URL:** `{site}/api/v1`
- **Official documentation:** [List Topics in a Channel](https://zulip.com/api/get-stream-topics)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `stream_id` | path | `number` | yes | The target channel ID. |

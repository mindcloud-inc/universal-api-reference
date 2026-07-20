# Get Channel by ID with Zulip

Retrieves a Zulip channel by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/streams/:stream_id`
- **Base URL:** `{site}/api/v1`
- **Official documentation:** [Get Channel by ID](https://zulip.com/api/get-stream-by-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `stream_id` | path | `number` | yes | The target channel ID. |

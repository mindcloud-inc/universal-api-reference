# Fetch Single Message with Zulip

Retrieves a single Zulip message by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/messages/:message_id`
- **Base URL:** `{site}/api/v1`
- **Official documentation:** [Fetch Single Message](https://zulip.com/api/get-message)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `message_id` | path | `number` | yes | The target message ID. |

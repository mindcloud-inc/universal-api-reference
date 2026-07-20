# Cancel Message with Wbiztool

Cancels a scheduled or queued message in Wbiztool.

## Endpoint

- **Method:** `POST`
- **Path:** `/cancel_msg/`
- **Base URL:** `https://wbiztool.com/api/v1`
- **Official documentation:** [Cancel Message](https://wbiztool.com/docs/cancel-message-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `msg_id` | body | `number` | yes | Unique message ID returned by the send or schedule message APIs. |

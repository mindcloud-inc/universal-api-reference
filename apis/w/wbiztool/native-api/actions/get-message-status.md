# Get Message Status with Wbiztool

Retrieves WhatsApp message delivery status from Wbiztool.

## Endpoint

- **Method:** `POST`
- **Path:** `/message/status/{{message_id}}/`
- **Base URL:** `https://wbiztool.com/api/v1`
- **Official documentation:** [Get Message Status](https://wbiztool.com/docs/message-status-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `message_id` | path | `number` | yes | Message ID to check in the URL path. |

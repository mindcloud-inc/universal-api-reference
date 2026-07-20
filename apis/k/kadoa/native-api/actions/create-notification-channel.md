# Create Notification Channel with Kadoa

## Endpoint

- **Method:** `POST`
- **Path:** `/v5/notifications/channels`
- **Base URL:** `https://api.kadoa.com`
- **Official documentation:** [Create Notification Channel](https://docs.kadoa.com/api-reference/notifications/create-notification-channel)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channelType` | body | `string` | yes | Type: EMAIL, SLACK, WEBHOOK, WEBSOCKET |
| `config` | body | `object` | yes | JSON config object |
| `name` | body | `string` | yes | Channel name |

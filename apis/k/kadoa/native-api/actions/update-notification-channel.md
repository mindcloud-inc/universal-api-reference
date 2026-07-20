# Update Notification Channel with Kadoa

## Endpoint

- **Method:** `PUT`
- **Path:** `/v5/notifications/channels/:channelId`
- **Base URL:** `https://api.kadoa.com`
- **Official documentation:** [Update Notification Channel](https://docs.kadoa.com/api-reference/notifications/update-notification-channel)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channelId` | path | `string` | yes | Channel ID |
| `channelType` | body | `string` | yes | Type: EMAIL, SLACK, WEBHOOK, WEBSOCKET |
| `config` | body | `object` | yes | JSON config object |
| `name` | body | `string` | yes | Channel name |

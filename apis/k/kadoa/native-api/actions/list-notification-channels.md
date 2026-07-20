# List Notification Channels with Kadoa

## Endpoint

- **Method:** `GET`
- **Path:** `/v5/notifications/channels`
- **Base URL:** `https://api.kadoa.com`
- **Official documentation:** [List Notification Channels](https://docs.kadoa.com/api-reference/notifications/get-notification-channels)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workflowId` | query | `string` | no | Filter by workflow ID |
| `includeConfigurations` | query | `boolean` | no | Include linked configs |

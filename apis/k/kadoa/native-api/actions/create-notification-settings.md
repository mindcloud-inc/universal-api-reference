# Create Notification Settings with Kadoa

## Endpoint

- **Method:** `POST`
- **Path:** `/v5/notifications/settings`
- **Base URL:** `https://api.kadoa.com`
- **Official documentation:** [Create Notification Settings](https://docs.kadoa.com/api-reference/notifications/create-notification-settings)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channelIds` | body | `list<string>` | no | JSON array of channel IDs Send multiple values as a array. |
| `enabled` | body | `boolean` | no | Enable notifications |
| `eventConfiguration` | body | `object` | no | JSON event config |
| `eventType` | body | `string` | yes | Event type |
| `workflowId` | body | `string` | no | Workflow ID (omit for workspace-level) |

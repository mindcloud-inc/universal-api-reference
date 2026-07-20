# Update Notification Settings with Kadoa

## Endpoint

- **Method:** `PUT`
- **Path:** `/v5/notifications/settings/:settingsId`
- **Base URL:** `https://api.kadoa.com`
- **Official documentation:** [Update Notification Settings](https://docs.kadoa.com/api-reference/notifications/update-notification-settings)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channelIds` | body | `list<string>` | no | JSON array of channel IDs Send multiple values as a array. |
| `enabled` | body | `boolean` | no | Enable or disable |
| `eventConfiguration` | body | `object` | no | JSON event config |
| `eventType` | body | `string` | no | Event type |
| `settingsId` | path | `string` | yes | Settings ID |

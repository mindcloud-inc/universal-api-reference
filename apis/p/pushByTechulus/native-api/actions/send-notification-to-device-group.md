# Send Notification to Device Group with Push by Techulus

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/notify/group/:groupId`
- **Base URL:** `https://push.techulus.com`
- **Official documentation:** [Send Notification to Device Group](https://docs.push.techulus.com/api-documentation-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | Device group ID. |
| `title` | body | `string` | yes | Notification title. |
| `body` | body | `string` | yes | Notification body text. |
| `sound` | body | `string` | no | Optional notification sound. |
| `channel` | body | `string` | no | Optional notification channel. |
| `link` | body | `string` | no | Optional URL opened by the notification. |
| `image` | body | `string` | no | Optional image URL. |
| `timeSensitive` | body | `boolean` | no | Deliver immediately on iOS even during Do Not Disturb. |

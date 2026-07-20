# Send Notification via GET with Push by Techulus

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/notify/:apiKey`
- **Base URL:** `https://push.techulus.com`
- **Official documentation:** [Send Notification via GET](https://docs.push.techulus.com/api-documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | query | `string` | yes | Notification title. |
| `body` | query | `string` | yes | Notification body text. |
| `sound` | query | `string` | no | Optional notification sound. |
| `channel` | query | `string` | no | Optional notification channel. |
| `link` | query | `string` | no | Optional URL opened by the notification. |
| `image` | query | `string` | no | Optional image URL. |
| `timeSensitive` | query | `boolean` | no | Deliver immediately on iOS even during Do Not Disturb. |

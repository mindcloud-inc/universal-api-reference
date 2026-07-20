# Send Notification via Path API Key with Push by Techulus

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/notify/:apiKey`
- **Base URL:** `https://push.techulus.com`
- **Official documentation:** [Send Notification via Path API Key](https://docs.push.techulus.com/api-documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | Notification title. |
| `body` | body | `string` | yes | Notification body text. |
| `sound` | body | `string` | no | Optional notification sound. |
| `channel` | body | `string` | no | Optional notification channel. |
| `link` | body | `string` | no | Optional URL opened by the notification. |
| `image` | body | `string` | no | Optional image URL. |
| `timeSensitive` | body | `boolean` | no | Deliver immediately on iOS even during Do Not Disturb. |

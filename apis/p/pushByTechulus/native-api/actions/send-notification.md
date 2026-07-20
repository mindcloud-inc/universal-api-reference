# Send Notification with Push by Techulus

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/notify`
- **Base URL:** `https://push.techulus.com`
- **Official documentation:** [Send Notification](https://docs.push.techulus.com/api-documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | Notification title. |
| `body` | body | `string` | yes | Notification body text. |
| `sound` | body | `string` | no | Optional notification sound. Valid values include default, arcade, correct, fail, harp, reveal, bubble, doorbell, flute, money, scifi, clear, elevator, guitar, and pop. |
| `channel` | body | `string` | no | Optional notification channel. Defaults to feed. |
| `link` | body | `string` | no | Optional notification link URL. |
| `image` | body | `string` | no | Optional notification image URL. |
| `timeSensitive` | body | `boolean` | no | Deliver immediately on iOS even during Do Not Disturb. |

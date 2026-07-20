# Send Viber Message with SMS.to

Sends a single Viber message through SMS.to.

## Endpoint

- **Method:** `POST`
- **Path:** `/viber/send`
- **Base URL:** `https://api.sms.to`
- **Official documentation:** [Send Viber Message](https://developers.sms.to/#fd60cb4c-3baa-4d9f-9e59-e93695357133)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `message` | body | `string` | no | Your message. |
| `to` | body | `string` | no | Phone number. |
| `callback_url` | body | `string` | no | A callback URL for message status updates. |
| `viber_image_url` | body | `string` | no | Image URL to Viber. |
| `viber_target_url` | body | `string` | no | Target URL. |
| `viber_caption` | body | `string` | no | Message caption. |

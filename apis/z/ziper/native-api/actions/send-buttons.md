# Send Buttons with Ziper

Sends a WhatsApp button message with Ziper.

## Endpoint

- **Method:** `POST`
- **Path:** `/send.php`
- **Base URL:** `https://ziper.io/api`
- **Official documentation:** [Send Buttons](https://documenter.getpostman.com/view/2881191/VUqmvyob)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `number` | query | `string` | yes | WhatsApp phone number in country-code plus phone-number format. |
| `text` | body | `string` | yes | Main button message text. |
| `footer` | body | `string` | no | Optional footer text for the button message. |
| `buttons[]` | body | `array<object>` | yes | Array of up to 3 button objects as documented by Ziper. |

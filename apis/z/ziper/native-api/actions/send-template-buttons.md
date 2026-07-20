# Send Template Buttons with Ziper

Sends a WhatsApp template-button message with Ziper.

## Endpoint

- **Method:** `POST`
- **Path:** `/send.php`
- **Base URL:** `https://ziper.io/api`
- **Official documentation:** [Send Template Buttons](https://documenter.getpostman.com/view/2881191/VUqmvyob)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `number` | query | `string` | yes | WhatsApp phone number in country-code plus phone-number format. |
| `text` | body | `string` | yes | Main template-button message text. |
| `footer` | body | `string` | no | Optional footer text for the template-button message. |
| `templateButtons[]` | body | `array<object>` | yes | Array of template button objects as documented by Ziper. |

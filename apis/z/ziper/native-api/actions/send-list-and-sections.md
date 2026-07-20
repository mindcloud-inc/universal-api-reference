# Send List And Sections with Ziper

Sends a WhatsApp list message with sections using Ziper.

## Endpoint

- **Method:** `POST`
- **Path:** `/send.php`
- **Base URL:** `https://ziper.io/api`
- **Official documentation:** [Send List And Sections](https://documenter.getpostman.com/view/2881191/VUqmvyob)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `number` | query | `string` | yes | WhatsApp phone number in country-code plus phone-number format. |
| `text` | body | `string` | yes | Main list message text. |
| `footer` | body | `string` | no | Optional footer text for the list message. |
| `title` | body | `string` | yes | Bold list title. |
| `buttonText` | body | `string` | yes | Text on the button that opens the list. |
| `sections[]` | body | `array<object>` | yes | List sections array as documented by Ziper. |

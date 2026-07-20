# Send Simple Text with Ziper

Sends a plain text WhatsApp message with Ziper.

## Endpoint

- **Method:** `POST`
- **Path:** `/send.php`
- **Base URL:** `https://ziper.io/api`
- **Official documentation:** [Send Simple Text](https://documenter.getpostman.com/view/2881191/VUqmvyob)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `number` | query | `string` | yes | WhatsApp phone number in country-code plus phone-number format. |
| `text` | body | `string` | yes | Message text to send. |

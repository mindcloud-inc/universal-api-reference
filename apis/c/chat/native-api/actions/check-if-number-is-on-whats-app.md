# Check If Number Is On WhatsApp with 2Chat

Finds whether a phone number is on WhatsApp in 2Chat.

## Endpoint

- **Method:** `GET`
- **Path:** `/whatsapp/check-number/:from_number/:number_to_check`
- **Base URL:** `https://api.p.2chat.io/open`
- **Official documentation:** [Check If Number Is On WhatsApp](https://developers.2chat.co/docs/API/WhatsApp/Web/check-number)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from_number` | path | `string` | yes | The WhatsApp number connected to 2Chat that performs the check. |
| `number_to_check` | path | `string` | yes | The phone number to verify on WhatsApp. |
| `extra-information` | query | `boolean` | no | Include extended WhatsApp profile information when available. |

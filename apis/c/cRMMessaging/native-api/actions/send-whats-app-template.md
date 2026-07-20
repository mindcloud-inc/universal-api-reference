# Send WhatsApp Template with CRM Messaging

Sends a WhatsApp template from CRM Messaging.

## Endpoint

- **Method:** `POST`
- **Path:** `/index.php/Api/sendMsg`
- **Base URL:** `https://app.crm-messaging.cloud`
- **Official documentation:** [Send WhatsApp Template](https://crm-messaging.cloud/docs/send-whatsapp-templates/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `to` | body | `string` | yes | Recipient phone number with country code. |
| `msg` | body | `string` | yes | WhatsApp template body. |
| `tempName` | body | `string` | yes | — |
| `mediaUrl` | body | `string` | no | — |
| `fromnum` | body | `string` | no | — |
| `lang` | body | `string` | no | — |
| `dlink` | body | `string` | no | — |
| `productId` | body | `string` | no | — |

# Send SMS with CRM Messaging

Sends an SMS from CRM Messaging.

## Endpoint

- **Method:** `POST`
- **Path:** `/index.php/Api/sendMsg`
- **Base URL:** `https://app.crm-messaging.cloud`
- **Official documentation:** [Send SMS](https://crm-messaging.cloud/docs/send-sms/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `to` | body | `string` | yes | Recipient phone number with country code. |
| `msg` | body | `string` | yes | SMS message body. |
| `mediaUrl` | body | `string` | no | — |
| `fromnum` | body | `string` | no | — |
| `channel` | body | `string` | no | — |
| `lang` | body | `string` | no | — |

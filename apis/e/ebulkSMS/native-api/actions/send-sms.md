# Send SMS with EbulkSMS

Sends an SMS with EbulkSMS.

## Endpoint

- **Method:** `POST`
- **Path:** `/sendsms.json`
- **Base URL:** `https://api.ebulksms.com`
- **Official documentation:** [Send SMS](https://www.ebulksms.com/pages/json-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `SMS` | body | `object` | no | Root SMS payload object. |
| `SMS.dndsender` | body | `number` | no | Use 1 to enable MTN DND delivery or 0 to disable it. |
| `SMS.message` | body | `object` | no | Message details object. |
| `SMS.message.flash` | body | `number` | no | Use 1 for flash SMS or 0 for a normal SMS. |
| `SMS.message.messagetext` | body | `string` | yes | The SMS content to send. |
| `SMS.message.sender` | body | `string` | yes | Sender name shown to recipients. |
| `SMS.recipients` | body | `object` | no | Recipients wrapper object. |
| `SMS.recipients.gsm[]` | body | `array<object>` | no | Recipient records. |
| `SMS.recipients.gsm[].msgid` | body | `string` | no | Optional unique ID for delivery-report tracking. |
| `SMS.recipients.gsm[].msidn` | body | `string` | yes | Recipient phone number in full international format. |

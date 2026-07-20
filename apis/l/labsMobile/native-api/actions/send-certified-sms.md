# Send Certified SMS with LabsMobile

Sends a certified SMS message with LabsMobile.

## Endpoint

- **Method:** `POST`
- **Path:** `/json/send`
- **Base URL:** `https://api.labsmobile.com`
- **Official documentation:** [Send Certified SMS](https://www.labsmobile.com/en/sms-api/api-versions/http-rest-post-json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `crt` | body | `string` | yes | Email address that receives the certificate PDF. |
| `message` | body | `string` | yes | Certified SMS body text. |
| `recipient[]` | body | `array<object>` | yes | Recipient array containing msisdn objects. |

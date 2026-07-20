# Send Unicode SMS with LabsMobile

Sends a Unicode SMS message with LabsMobile.

## Endpoint

- **Method:** `POST`
- **Path:** `/json/send`
- **Base URL:** `https://api.labsmobile.com`
- **Official documentation:** [Send Unicode SMS](https://www.labsmobile.com/en/sms-api/api-versions/http-rest-post-json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `message` | body | `string` | yes | Unicode SMS body text. |
| `recipient[]` | body | `array<object>` | yes | Recipient array containing msisdn objects. |

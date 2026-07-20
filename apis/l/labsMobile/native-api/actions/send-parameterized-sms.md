# Send Parameterized SMS with LabsMobile

Sends a parameterized SMS message with LabsMobile.

## Endpoint

- **Method:** `POST`
- **Path:** `/json/send`
- **Base URL:** `https://api.labsmobile.com`
- **Official documentation:** [Send Parameterized SMS](https://www.labsmobile.com/en/sms-api/api-versions/http-rest-post-json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `message` | body | `string` | yes | SMS body text containing placeholder tokens. |
| `parameters[]` | body | `array<object>` | yes | Parameter replacement object array. |
| `recipient[]` | body | `array<object>` | yes | Recipient array containing msisdn objects. |

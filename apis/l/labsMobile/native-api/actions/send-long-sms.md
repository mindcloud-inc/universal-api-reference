# Send Long SMS with LabsMobile

Sends a concatenated long SMS message with LabsMobile.

## Endpoint

- **Method:** `POST`
- **Path:** `/json/send`
- **Base URL:** `https://api.labsmobile.com`
- **Official documentation:** [Send Long SMS](https://www.labsmobile.com/en/sms-api/api-versions/http-rest-post-json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `message` | body | `string` | yes | Long SMS body text. |
| `recipient[]` | body | `array<object>` | yes | Recipient array containing msisdn objects. |

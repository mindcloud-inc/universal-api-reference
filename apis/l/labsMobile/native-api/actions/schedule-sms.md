# Schedule SMS with LabsMobile

Schedules an SMS message in LabsMobile.

## Endpoint

- **Method:** `POST`
- **Path:** `/json/send`
- **Base URL:** `https://api.labsmobile.com`
- **Official documentation:** [Schedule SMS](https://www.labsmobile.com/en/sms-api/api-versions/http-rest-post-json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `message` | body | `string` | yes | Scheduled SMS body text. |
| `recipient[]` | body | `array<object>` | yes | Recipient array containing msisdn objects. |
| `scheduled` | body | `date` | yes | Send time in GMT using YYYY-MM-DD HH:MM:SS. |
| `subid` | body | `string` | no | Identifier for the scheduled send. |

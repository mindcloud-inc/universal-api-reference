# Cancel Scheduled SMS with LabsMobile

Cancels a scheduled SMS message in LabsMobile.

## Endpoint

- **Method:** `POST`
- **Path:** `/json/scheduled`
- **Base URL:** `https://api.labsmobile.com`
- **Official documentation:** [Cancel Scheduled SMS](https://www.labsmobile.com/en/sms-api/api-versions/http-rest-post-json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subid` | body | `string` | yes | Identifier for the scheduled send. |

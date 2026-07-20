# Update Calendar with ECAL

Updates an existing calendar in ECAL.

## Endpoint

- **Method:** `PUT`
- **Path:** `/calendar/:calendarId`
- **Base URL:** `https://api.ecal.com/apiv2`
- **Official documentation:** [Update Calendar](https://docs.ecal.com/reference/apiv2/calendar.html#put-apiv2calendarid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `calendarId` | path | `string` | yes | ECAL calendar ID to update. |
| `requestBody` | body | `object` | yes | JSON object matching ECAL's update calendar payload. |

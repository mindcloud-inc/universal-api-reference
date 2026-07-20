# Get Specific Attendance Entry with Zoho People

Retrieves an attendance entry from Zoho People.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v3/attendance/entries/:entryId`
- **Base URL:** `https://people.zoho.com`
- **Official documentation:** [Get Specific Attendance Entry](https://www.zoho.com/people/api/v3/attendance/entries/get-specific.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entryId` | path | `string` | yes | Attendance entry ID. |
| `date` | query | `string` | no | Required only when the origin day does not fall within the current year. |

# List Upcoming Events with WaiverFile

Retrieves upcoming events from WaiverFile.

## Endpoint

- **Method:** `GET`
- **Path:** `/GetUpcomingEvents`
- **Base URL:** `https://api.waiverfile.com/api/v1`
- **Official documentation:** [List Upcoming Events](https://api.waiverfile.com/swagger/ui/index)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `startDateUTC` | query | `date` | yes |
| `endDateUTC` | query | `date` | yes |

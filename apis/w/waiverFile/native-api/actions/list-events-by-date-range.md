# List Events by Date Range with WaiverFile

Retrieves events from WaiverFile by date range.

## Endpoint

- **Method:** `GET`
- **Path:** `/GetEventsByDateRange`
- **Base URL:** `https://api.waiverfile.com/api/v1`
- **Official documentation:** [List Events by Date Range](https://api.waiverfile.com/swagger/ui/index)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `startDateUTC` | query | `date` | yes |
| `endDateUTC` | query | `date` | yes |

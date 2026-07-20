# List Events by Category with WaiverFile

Retrieves events from WaiverFile by category.

## Endpoint

- **Method:** `GET`
- **Path:** `/GetEventsByCategory`
- **Base URL:** `https://api.waiverfile.com/api/v1`
- **Official documentation:** [List Events by Category](https://api.waiverfile.com/swagger/ui/index)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `eventCategoryID` | query | `string` | yes |
| `startDateUTC` | query | `date` | yes |
| `endDateUTC` | query | `date` | yes |

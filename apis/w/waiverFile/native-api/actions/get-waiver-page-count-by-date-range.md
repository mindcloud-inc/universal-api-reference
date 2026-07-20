# Get Waiver Page Count by Date Range with WaiverFile

Retrieves waiver page count from WaiverFile by date range.

## Endpoint

- **Method:** `GET`
- **Path:** `/GetAllWaiversByDateRangePageCount`
- **Base URL:** `https://api.waiverfile.com/api/v1`
- **Official documentation:** [Get Waiver Page Count by Date Range](https://api.waiverfile.com/swagger/ui/index)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `startDate` | query | `date` | yes |
| `endDate` | query | `date` | yes |

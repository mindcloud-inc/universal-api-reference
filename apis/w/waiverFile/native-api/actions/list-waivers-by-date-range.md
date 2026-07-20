# List Waivers by Date Range with WaiverFile

Retrieves waivers from WaiverFile by date range.

## Endpoint

- **Method:** `GET`
- **Path:** `/GetAllWaiversByDateRange`
- **Base URL:** `https://api.waiverfile.com/api/v1`
- **Official documentation:** [List Waivers by Date Range](https://api.waiverfile.com/swagger/ui/index)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `startDate` | query | `date` | yes |
| `endDate` | query | `date` | yes |
| `pageIndex` | query | `number` | yes |
| `pageSize` | query | `number` | yes |

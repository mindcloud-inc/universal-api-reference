# List Waiver Data with WaiverFile

Retrieves waiver data from WaiverFile.

## Endpoint

- **Method:** `GET`
- **Path:** `/GetWaiverData`
- **Base URL:** `https://api.waiverfile.com/api/v1`
- **Official documentation:** [List Waiver Data](https://api.waiverfile.com/swagger/ui/index)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `startDate` | query | `date` | yes |
| `endDate` | query | `date` | yes |
| `includeCustomColumns` | query | `boolean` | yes |
| `consolidateParticipants` | query | `boolean` | yes |
| `pageIndex` | query | `number` | yes |
| `pageSize` | query | `number` | yes |

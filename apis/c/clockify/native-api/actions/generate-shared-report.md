# Generate Shared Report with Clockify

Generates a shared report in Clockify.

## Endpoint

- **Method:** `GET`
- **Path:** `shared-reports/:id`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Generate Shared Report](https://docs.developer.clockify.me/#tag/Shared-Report/operation/generateSharedReportV1)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `dateRangeEnd` | query | `string` | no |
| `dateRangeStart` | query | `string` | no |
| `exportType` | query | `string` | no |
| `id` | path | `string` | yes |
| `page` | query | `number` | no |
| `pageSize` | query | `number` | no |
| `sortColumn` | query | `string` | no |
| `sortOrder` | query | `string` | no |

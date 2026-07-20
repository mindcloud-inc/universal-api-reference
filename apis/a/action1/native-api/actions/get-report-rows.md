# Get Report Rows with Action1

Retrieves report rows from Action1 for a report.

## Endpoint

- **Method:** `GET`
- **Path:** `/reportdata/:orgId/:reportId/data`
- **Base URL:** `https://app.action1.com/api/3.0`
- **Official documentation:** [Get Report Rows](https://app.action1.com/apidocs/#/Reports.%20Report%20Data/reportdata_orgId_reportId_data_get)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orgId` | path | `string` | yes | Provide an organization ID. |
| `reportId` | path | `string` | yes | Provide a specific report ID. |

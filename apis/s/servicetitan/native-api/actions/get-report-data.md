# Get Report Data with ServiceTitan

Retrieves report data from ServiceTitan.

## Endpoint

- **Method:** `POST`
- **Path:** `reporting/v2/tenant/{tenant}/report-category/:report_category/reports/:reportId/data`
- **Base URL:** `https://{baseUrl}/`
- **Official documentation:** [Get Report Data](https://developer.servicetitan.io/docs/apis/tenant-reporting-v2/endpoints/ReportCategoryReports_GetData)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `report_category` | path | `string` | yes | ID of category taken from the category list endpoint. |
| `reportId` | path | `number` | yes | ID of report within the category. |
| `parameters[]` | body | `array<object>` | yes | List of name/value input parameters for the report. |
| `includeTotal` | query | `boolean` | no | Whether total count should be returned. |

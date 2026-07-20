# List Reports with ServiceTitan

Retrieves reports from ServiceTitan by category.

## Endpoint

- **Method:** `GET`
- **Path:** `reporting/v2/tenant/{tenant}/report-category/:report_category/reports`
- **Base URL:** `https://{baseUrl}/`
- **Official documentation:** [List Reports](https://developer.servicetitan.io/docs/apis/tenant-reporting-v2/endpoints/ReportCategoryReports_GetReports)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `report_category` | path | `string` | yes | ID of category taken from the category list endpoint. |
| `includeTotal` | query | `boolean` | no | Whether total count should be returned. |

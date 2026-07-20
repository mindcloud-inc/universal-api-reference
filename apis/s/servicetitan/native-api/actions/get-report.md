# Get Report with ServiceTitan

Retrieves a report definition from ServiceTitan.

## Endpoint

- **Method:** `GET`
- **Path:** `reporting/v2/tenant/{tenant}/report-category/:report_category/reports/:reportId`
- **Base URL:** `https://{baseUrl}/`
- **Official documentation:** [Get Report](https://developer.servicetitan.io/docs/apis/tenant-reporting-v2/endpoints/ReportCategoryReports_Get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `report_category` | path | `string` | yes | ID of category taken from the category list endpoint. |
| `reportId` | path | `number` | yes | ID of report within the category. |

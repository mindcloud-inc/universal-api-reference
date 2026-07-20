# List Report Categories with ServiceTitan

Retrieves report categories from ServiceTitan.

## Endpoint

- **Method:** `GET`
- **Path:** `reporting/v2/tenant/{tenant}/report-categories`
- **Base URL:** `https://{baseUrl}/`
- **Official documentation:** [List Report Categories](https://developer.servicetitan.io/docs/apis/tenant-reporting-v2/endpoints/ReportCategories_GetCategories)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `includeTotal` | query | `boolean` | no | Whether total count should be returned. |

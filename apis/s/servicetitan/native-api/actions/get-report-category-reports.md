# Get Report Category Reports with ServiceTitan

## Endpoint

- **Method:** `POST`
- **Path:** `reporting/v2/tenant/{tenant}/report-category/:category/reports/:reportId/data`
- **Base URL:** `https://{baseUrl}/`
- **Official documentation:** [Get Report Category Reports](https://developer.servicetitan.io/docs/apis/tenant-forms-v2/endpoints/Jobs_CreateAttachment)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `reportId` | path | `string` | yes |
| `category` | path | `string` | yes |
| `parameters` | body | `string` | no |

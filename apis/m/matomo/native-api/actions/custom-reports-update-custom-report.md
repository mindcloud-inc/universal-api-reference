# CustomReports update Custom Report with Matomo

## Endpoint

- **Method:** `POST`
- **Path:** `/index.php`
- **Base URL:** `https://mindcloud.matomo.cloud`
- **Official documentation:** [CustomReports update Custom Report](https://developer.matomo.org/api-reference/reporting-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `idSite` | body | `number` | yes | Matomo API parameter. |
| `idCustomReport` | body | `string` | yes | Matomo API parameter. |
| `name` | body | `string` | yes | Matomo API parameter. |
| `reportType` | body | `string` | yes | Matomo API parameter. |
| `metricIds` | body | `string` | yes | Matomo API parameter. |
| `categoryId` | body | `string` | no | Matomo API parameter. |
| `dimensionIds` | body | `string` | no | Matomo API parameter. |
| `subcategoryId` | body | `string` | no | Matomo API parameter. |
| `description` | body | `string` | no | Matomo API parameter. |
| `segmentFilter` | body | `string` | no | Matomo API parameter. |
| `subCategoryReportIds` | body | `string` | no | Matomo API parameter. |
| `multipleIdSites` | body | `string` | no | Matomo API parameter. |

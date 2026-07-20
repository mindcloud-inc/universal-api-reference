# ScheduledReports update Report with Matomo

## Endpoint

- **Method:** `POST`
- **Path:** `/index.php`
- **Base URL:** `https://mindcloud.matomo.cloud`
- **Official documentation:** [ScheduledReports update Report](https://developer.matomo.org/api-reference/reporting-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `idReport` | body | `string` | yes | Matomo API parameter. |
| `idSite` | body | `number` | yes | Matomo API parameter. |
| `description` | body | `string` | yes | Matomo API parameter. |
| `period` | body | `string` | yes | Matomo API parameter. |
| `hour` | body | `string` | yes | Matomo API parameter. |
| `reportType` | body | `string` | yes | Matomo API parameter. |
| `reportFormat` | body | `string` | yes | Matomo API parameter. |
| `reports` | body | `string` | yes | Matomo API parameter. |
| `parameters` | body | `string` | yes | Matomo API parameter. |
| `idSegment` | body | `string` | no | Matomo API parameter. |
| `evolutionPeriodFor` | body | `string` | no | Matomo API parameter. |
| `evolutionPeriodN` | body | `string` | no | Matomo API parameter. |
| `periodParam` | body | `string` | no | Matomo API parameter. |

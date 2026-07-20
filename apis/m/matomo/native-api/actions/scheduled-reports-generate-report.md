# ScheduledReports generate Report with Matomo

## Endpoint

- **Method:** `POST`
- **Path:** `/index.php`
- **Base URL:** `https://mindcloud.matomo.cloud`
- **Official documentation:** [ScheduledReports generate Report](https://developer.matomo.org/api-reference/reporting-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `idReport` | body | `string` | yes | Matomo API parameter. |
| `date` | body | `string` | yes | Matomo API parameter. |
| `language` | body | `string` | no | Matomo API parameter. |
| `outputType` | body | `string` | no | Matomo API parameter. |
| `period` | body | `string` | no | Matomo API parameter. |
| `reportFormat` | body | `string` | no | Matomo API parameter. |
| `parameters` | body | `string` | no | Matomo API parameter. |

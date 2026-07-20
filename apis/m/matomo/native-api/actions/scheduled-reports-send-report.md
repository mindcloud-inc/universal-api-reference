# ScheduledReports send Report with Matomo

## Endpoint

- **Method:** `POST`
- **Path:** `/index.php`
- **Base URL:** `https://mindcloud.matomo.cloud`
- **Official documentation:** [ScheduledReports send Report](https://developer.matomo.org/api-reference/reporting-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `idReport` | body | `string` | yes | Matomo API parameter. |
| `period` | body | `string` | no | Matomo API parameter. |
| `date` | body | `string` | no | Matomo API parameter. |
| `force` | body | `boolean` | no | Matomo API parameter. |

# API get Processed Report with Matomo

## Endpoint

- **Method:** `POST`
- **Path:** `/index.php`
- **Base URL:** `https://mindcloud.matomo.cloud`
- **Official documentation:** [API get Processed Report](https://developer.matomo.org/api-reference/reporting-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `idSite` | body | `number` | yes | Matomo API parameter. |
| `period` | body | `string` | yes | Matomo API parameter. |
| `date` | body | `string` | yes | Matomo API parameter. |
| `apiModule` | body | `string` | yes | Matomo API parameter. |
| `apiAction` | body | `string` | yes | Matomo API parameter. |
| `segment` | body | `string` | no | Matomo API parameter. |
| `apiParameters` | body | `string` | no | Matomo API parameter. |
| `idGoal` | body | `number` | no | Matomo API parameter. |
| `language` | body | `string` | no | Matomo API parameter. |
| `showTimer` | body | `boolean` | no | Matomo API parameter. |
| `hideMetricsDoc` | body | `boolean` | no | Matomo API parameter. |
| `idSubtable` | body | `number` | no | Matomo API parameter. |
| `showRawMetrics` | body | `boolean` | no | Matomo API parameter. |
| `format_metrics` | body | `string` | no | Matomo API parameter. |
| `idDimension` | body | `string` | no | Matomo API parameter. |

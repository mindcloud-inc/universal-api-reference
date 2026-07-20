# API get Row Evolution with Matomo

## Endpoint

- **Method:** `POST`
- **Path:** `/index.php`
- **Base URL:** `https://mindcloud.matomo.cloud`
- **Official documentation:** [API get Row Evolution](https://developer.matomo.org/api-reference/reporting-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `idSite` | body | `number` | yes | Matomo API parameter. |
| `period` | body | `string` | yes | Matomo API parameter. |
| `date` | body | `string` | yes | Matomo API parameter. |
| `apiModule` | body | `string` | yes | Matomo API parameter. |
| `apiAction` | body | `string` | yes | Matomo API parameter. |
| `label` | body | `string` | no | Matomo API parameter. |
| `segment` | body | `string` | no | Matomo API parameter. |
| `column` | body | `string` | no | Matomo API parameter. |
| `language` | body | `string` | no | Matomo API parameter. |
| `idGoal` | body | `number` | no | Matomo API parameter. |
| `legendAppendMetric` | body | `string` | no | Matomo API parameter. |
| `labelUseAbsoluteUrl` | body | `string` | no | Matomo API parameter. |
| `idDimension` | body | `string` | no | Matomo API parameter. |
| `labelSeries` | body | `string` | no | Matomo API parameter. |
| `showGoalMetricsForGoal` | body | `boolean` | no | Matomo API parameter. |

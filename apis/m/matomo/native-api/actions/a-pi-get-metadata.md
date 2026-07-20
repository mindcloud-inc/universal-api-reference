# API get Metadata with Matomo

## Endpoint

- **Method:** `POST`
- **Path:** `/index.php`
- **Base URL:** `https://mindcloud.matomo.cloud`
- **Official documentation:** [API get Metadata](https://developer.matomo.org/api-reference/reporting-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `idSite` | body | `number` | yes | Matomo API parameter. |
| `apiModule` | body | `string` | yes | Matomo API parameter. |
| `apiAction` | body | `string` | yes | Matomo API parameter. |
| `apiParameters` | body | `string` | no | Matomo API parameter. |
| `language` | body | `string` | no | Matomo API parameter. |
| `period` | body | `string` | no | Matomo API parameter. |
| `date` | body | `string` | no | Matomo API parameter. |
| `hideMetricsDoc` | body | `boolean` | no | Matomo API parameter. |
| `showSubtableReports` | body | `boolean` | no | Matomo API parameter. |

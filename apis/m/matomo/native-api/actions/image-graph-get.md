# ImageGraph get with Matomo

## Endpoint

- **Method:** `POST`
- **Path:** `/index.php`
- **Base URL:** `https://mindcloud.matomo.cloud`
- **Official documentation:** [ImageGraph get](https://developer.matomo.org/api-reference/reporting-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `idSite` | body | `number` | yes | Matomo API parameter. |
| `period` | body | `string` | yes | Matomo API parameter. |
| `date` | body | `string` | yes | Matomo API parameter. |
| `apiModule` | body | `string` | yes | Matomo API parameter. |
| `apiAction` | body | `string` | yes | Matomo API parameter. |
| `graphType` | body | `string` | no | Matomo API parameter. |
| `outputType` | body | `string` | no | Matomo API parameter. |
| `columns` | body | `string` | no | Matomo API parameter. |
| `labels` | body | `string` | no | Matomo API parameter. |
| `showLegend` | body | `boolean` | no | Matomo API parameter. |
| `width` | body | `string` | no | Matomo API parameter. |
| `height` | body | `string` | no | Matomo API parameter. |
| `fontSize` | body | `string` | no | Matomo API parameter. |
| `legendFontSize` | body | `string` | no | Matomo API parameter. |
| `aliasedGraph` | body | `string` | no | Matomo API parameter. |
| `idGoal` | body | `number` | no | Matomo API parameter. |
| `colors` | body | `string` | no | Matomo API parameter. |
| `textColor` | body | `string` | no | Matomo API parameter. |
| `backgroundColor` | body | `string` | no | Matomo API parameter. |
| `gridColor` | body | `string` | no | Matomo API parameter. |
| `idSubtable` | body | `number` | no | Matomo API parameter. |
| `legendAppendMetric` | body | `string` | no | Matomo API parameter. |
| `segment` | body | `string` | no | Matomo API parameter. |
| `idDimension` | body | `string` | no | Matomo API parameter. |

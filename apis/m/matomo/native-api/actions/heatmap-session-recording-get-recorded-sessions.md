# HeatmapSessionRecording get Recorded Sessions with Matomo

## Endpoint

- **Method:** `POST`
- **Path:** `/index.php`
- **Base URL:** `https://mindcloud.matomo.cloud`
- **Official documentation:** [HeatmapSessionRecording get Recorded Sessions](https://developer.matomo.org/api-reference/reporting-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `idSite` | body | `number` | yes | Matomo API parameter. |
| `period` | body | `string` | yes | Matomo API parameter. |
| `date` | body | `string` | yes | Matomo API parameter. |
| `idSiteHsr` | body | `number` | yes | Matomo API parameter. |
| `segment` | body | `string` | no | Matomo API parameter. |
| `idSubtable` | body | `number` | no | Matomo API parameter. |

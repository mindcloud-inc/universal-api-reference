# HeatmapSessionRecording duplicate Heatmap with Matomo

## Endpoint

- **Method:** `POST`
- **Path:** `/index.php`
- **Base URL:** `https://mindcloud.matomo.cloud`
- **Official documentation:** [HeatmapSessionRecording duplicate Heatmap](https://developer.matomo.org/api-reference/reporting-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `idSite` | body | `number` | yes | Matomo API parameter. |
| `idSiteHsr` | body | `number` | yes | Matomo API parameter. |
| `idDestinationSites` | body | `string` | no | Matomo API parameter. |

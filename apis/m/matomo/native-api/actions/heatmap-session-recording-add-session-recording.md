# HeatmapSessionRecording add Session Recording with Matomo

## Endpoint

- **Method:** `POST`
- **Path:** `/index.php`
- **Base URL:** `https://mindcloud.matomo.cloud`
- **Official documentation:** [HeatmapSessionRecording add Session Recording](https://developer.matomo.org/api-reference/reporting-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `idSite` | body | `number` | yes | Matomo API parameter. |
| `name` | body | `string` | yes | Matomo API parameter. |
| `matchPageRules` | body | `boolean` | no | Matomo API parameter. |
| `sampleLimit` | body | `string` | no | Matomo API parameter. |
| `sampleRate` | body | `string` | no | Matomo API parameter. |
| `minSessionTime` | body | `string` | no | Matomo API parameter. |
| `requiresActivity` | body | `string` | no | Matomo API parameter. |
| `captureKeystrokes` | body | `string` | no | Matomo API parameter. |

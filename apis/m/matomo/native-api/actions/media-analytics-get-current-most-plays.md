# MediaAnalytics get Current Most Plays with Matomo

## Endpoint

- **Method:** `POST`
- **Path:** `/index.php`
- **Base URL:** `https://mindcloud.matomo.cloud`
- **Official documentation:** [MediaAnalytics get Current Most Plays](https://developer.matomo.org/api-reference/reporting-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `idSite` | body | `number` | yes | Matomo API parameter. |
| `lastMinutes` | body | `string` | yes | Matomo API parameter. |
| `filter_limit` | body | `number` | no | Matomo API parameter. |
| `segment` | body | `string` | no | Matomo API parameter. |

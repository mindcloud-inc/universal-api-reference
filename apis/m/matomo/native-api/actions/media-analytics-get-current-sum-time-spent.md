# MediaAnalytics get Current Sum Time Spent with Matomo

## Endpoint

- **Method:** `POST`
- **Path:** `/index.php`
- **Base URL:** `https://mindcloud.matomo.cloud`
- **Official documentation:** [MediaAnalytics get Current Sum Time Spent](https://developer.matomo.org/api-reference/reporting-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `idSite` | body | `number` | yes | Matomo API parameter. |
| `lastMinutes` | body | `string` | yes | Matomo API parameter. |
| `segment` | body | `string` | no | Matomo API parameter. |

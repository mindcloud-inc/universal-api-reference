# CrashAnalytics get Last Crashes Overview with Matomo

## Endpoint

- **Method:** `POST`
- **Path:** `/index.php`
- **Base URL:** `https://mindcloud.matomo.cloud`
- **Official documentation:** [CrashAnalytics get Last Crashes Overview](https://developer.matomo.org/api-reference/reporting-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `idSite` | body | `number` | yes | Matomo API parameter. |
| `segment` | body | `string` | no | Matomo API parameter. |
| `lastMinutes` | body | `string` | no | Matomo API parameter. |

# CrashAnalytics get Crash Visit Context with Matomo

## Endpoint

- **Method:** `POST`
- **Path:** `/index.php`
- **Base URL:** `https://mindcloud.matomo.cloud`
- **Official documentation:** [CrashAnalytics get Crash Visit Context](https://developer.matomo.org/api-reference/reporting-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `idLogCrash` | body | `string` | yes | Matomo API parameter. |
| `idSite` | body | `number` | yes | Matomo API parameter. |
| `period` | body | `string` | yes | Matomo API parameter. |
| `date` | body | `string` | yes | Matomo API parameter. |
| `segment` | body | `string` | no | Matomo API parameter. |
| `filter_limit` | body | `number` | no | Matomo API parameter. |
| `filter_offset` | body | `number` | no | Matomo API parameter. |
| `fetchRecentActions` | body | `string` | no | Matomo API parameter. |

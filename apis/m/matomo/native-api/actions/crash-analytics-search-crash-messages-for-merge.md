# CrashAnalytics search Crash Messages For Merge with Matomo

## Endpoint

- **Method:** `POST`
- **Path:** `/index.php`
- **Base URL:** `https://mindcloud.matomo.cloud`
- **Official documentation:** [CrashAnalytics search Crash Messages For Merge](https://developer.matomo.org/api-reference/reporting-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `idSite` | body | `number` | yes | Matomo API parameter. |
| `resourceUri` | body | `string` | no | Matomo API parameter. |
| `searchTerm` | body | `string` | no | Matomo API parameter. |
| `limit` | body | `number` | no | Matomo API parameter. |
| `offset` | body | `number` | no | Matomo API parameter. |
| `excludeIdLogCrashes` | body | `string` | no | Matomo API parameter. |

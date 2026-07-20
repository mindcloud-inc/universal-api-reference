# CrashAnalytics set Ignore Crash with Matomo

## Endpoint

- **Method:** `POST`
- **Path:** `/index.php`
- **Base URL:** `https://mindcloud.matomo.cloud`
- **Official documentation:** [CrashAnalytics set Ignore Crash](https://developer.matomo.org/api-reference/reporting-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `idSite` | body | `number` | yes | Matomo API parameter. |
| `idLogCrash` | body | `string` | yes | Matomo API parameter. |
| `ignore` | body | `string` | no | Matomo API parameter. |

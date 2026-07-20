# CrashAnalytics get All Crashes with Matomo

## Endpoint

- **Method:** `POST`
- **Path:** `/index.php`
- **Base URL:** `https://mindcloud.matomo.cloud`
- **Official documentation:** [CrashAnalytics get All Crashes](https://developer.matomo.org/api-reference/reporting-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `idSite` | body | `number` | yes | Matomo API parameter. |
| `filter_sort_column` | body | `string` | no | Matomo API parameter. |
| `filter_sort_order` | body | `string` | no | Matomo API parameter. |
| `filter_limit` | body | `number` | no | Matomo API parameter. |
| `filter_offset` | body | `number` | no | Matomo API parameter. |

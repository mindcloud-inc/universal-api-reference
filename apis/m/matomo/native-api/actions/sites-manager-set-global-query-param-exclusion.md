# SitesManager set Global Query Param Exclusion with Matomo

## Endpoint

- **Method:** `POST`
- **Path:** `/index.php`
- **Base URL:** `https://mindcloud.matomo.cloud`
- **Official documentation:** [SitesManager set Global Query Param Exclusion](https://developer.matomo.org/api-reference/reporting-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `exclusionType` | body | `string` | yes | Matomo API parameter. |
| `?string queryParamsToExclude` | body | `string` | yes | Matomo API parameter. |

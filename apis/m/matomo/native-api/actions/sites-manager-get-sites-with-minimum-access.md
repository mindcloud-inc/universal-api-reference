# SitesManager get Sites With Minimum Access with Matomo

## Endpoint

- **Method:** `POST`
- **Path:** `/index.php`
- **Base URL:** `https://mindcloud.matomo.cloud`
- **Official documentation:** [SitesManager get Sites With Minimum Access](https://developer.matomo.org/api-reference/reporting-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `permission` | body | `string` | yes | Matomo API parameter. |
| `?string pattern` | body | `string` | yes | Matomo API parameter. |
| `?int limit` | body | `string` | yes | Matomo API parameter. |
| `sitesToExclude` | body | `string` | no | Matomo API parameter. |
| `siteTypesToExclude` | body | `string` | no | Matomo API parameter. |

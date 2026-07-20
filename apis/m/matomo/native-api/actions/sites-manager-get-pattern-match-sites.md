# SitesManager get Pattern Match Sites with Matomo

## Endpoint

- **Method:** `POST`
- **Path:** `/index.php`
- **Base URL:** `https://mindcloud.matomo.cloud`
- **Official documentation:** [SitesManager get Pattern Match Sites](https://developer.matomo.org/api-reference/reporting-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pattern` | body | `string` | yes | Matomo API parameter. |
| `limit` | body | `number` | no | Matomo API parameter. |
| `sitesToExclude` | body | `string` | no | Matomo API parameter. |

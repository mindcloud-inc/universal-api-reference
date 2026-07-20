# MultiSites get All With Groups with Matomo

## Endpoint

- **Method:** `POST`
- **Path:** `/index.php`
- **Base URL:** `https://mindcloud.matomo.cloud`
- **Official documentation:** [MultiSites get All With Groups](https://developer.matomo.org/api-reference/reporting-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `?string period` | body | `string` | yes | Matomo API parameter. |
| `?string date` | body | `string` | yes | Matomo API parameter. |
| `?string segment` | body | `string` | yes | Matomo API parameter. |
| `pattern` | body | `string` | no | Matomo API parameter. |
| `filter_limit` | body | `number` | no | Matomo API parameter. |

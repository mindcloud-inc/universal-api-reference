# Dashboard create New Dashboard For User with Matomo

## Endpoint

- **Method:** `POST`
- **Path:** `/index.php`
- **Base URL:** `https://mindcloud.matomo.cloud`
- **Official documentation:** [Dashboard create New Dashboard For User](https://developer.matomo.org/api-reference/reporting-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `login` | body | `string` | yes | Matomo API parameter. |
| `dashboardName` | body | `string` | no | Matomo API parameter. |
| `addDefaultWidgets` | body | `string` | no | Matomo API parameter. |

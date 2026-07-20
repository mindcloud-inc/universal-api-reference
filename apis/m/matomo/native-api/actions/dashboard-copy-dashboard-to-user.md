# Dashboard copy Dashboard To User with Matomo

## Endpoint

- **Method:** `POST`
- **Path:** `/index.php`
- **Base URL:** `https://mindcloud.matomo.cloud`
- **Official documentation:** [Dashboard copy Dashboard To User](https://developer.matomo.org/api-reference/reporting-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `idDashboard` | body | `string` | yes | Matomo API parameter. |
| `copyToUser` | body | `string` | yes | Matomo API parameter. |
| `dashboardName` | body | `string` | no | Matomo API parameter. |

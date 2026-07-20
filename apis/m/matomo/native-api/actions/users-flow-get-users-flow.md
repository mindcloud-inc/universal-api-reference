# UsersFlow get Users Flow with Matomo

## Endpoint

- **Method:** `POST`
- **Path:** `/index.php`
- **Base URL:** `https://mindcloud.matomo.cloud`
- **Official documentation:** [UsersFlow get Users Flow](https://developer.matomo.org/api-reference/reporting-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `idSite` | body | `number` | yes | Matomo API parameter. |
| `period` | body | `string` | yes | Matomo API parameter. |
| `date` | body | `string` | yes | Matomo API parameter. |
| `limitActionsPerStep` | body | `string` | no | Matomo API parameter. |
| `exploreStep` | body | `string` | no | Matomo API parameter. |
| `exploreUrl` | body | `string` | no | Matomo API parameter. |
| `segment` | body | `string` | no | Matomo API parameter. |
| `expanded` | body | `boolean` | no | Matomo API parameter. |
| `dataSource` | body | `string` | no | Matomo API parameter. |

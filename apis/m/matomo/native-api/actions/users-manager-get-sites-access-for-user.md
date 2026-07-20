# UsersManager get Sites Access For User with Matomo

## Endpoint

- **Method:** `POST`
- **Path:** `/index.php`
- **Base URL:** `https://mindcloud.matomo.cloud`
- **Official documentation:** [UsersManager get Sites Access For User](https://developer.matomo.org/api-reference/reporting-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userLogin` | body | `string` | yes | Matomo API parameter. |
| `limit` | body | `number` | no | Matomo API parameter. |
| `offset` | body | `number` | no | Matomo API parameter. |
| `filter_search` | body | `string` | no | Matomo API parameter. |
| `filter_access` | body | `string` | no | Matomo API parameter. |

# UsersManager add Capabilities with Matomo

## Endpoint

- **Method:** `POST`
- **Path:** `/index.php`
- **Base URL:** `https://mindcloud.matomo.cloud`
- **Official documentation:** [UsersManager add Capabilities](https://developer.matomo.org/api-reference/reporting-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userLogin` | body | `string` | yes | Matomo API parameter. |
| `capabilities` | body | `string` | yes | Matomo API parameter. |
| `idSites` | body | `string` | yes | Matomo API parameter. |

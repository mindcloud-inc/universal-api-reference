# UsersManager set User Access with Matomo

## Endpoint

- **Method:** `POST`
- **Path:** `/index.php`
- **Base URL:** `https://mindcloud.matomo.cloud`
- **Official documentation:** [UsersManager set User Access](https://developer.matomo.org/api-reference/reporting-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userLogin` | body | `string` | yes | Matomo API parameter. |
| `access` | body | `string` | yes | Matomo API parameter. |
| `idSites` | body | `string` | yes | Matomo API parameter. |
| `passwordConfirmation` | body | `string` | no | Matomo API parameter. |

# UsersManager create App Specific Token Auth with Matomo

## Endpoint

- **Method:** `POST`
- **Path:** `/index.php`
- **Base URL:** `https://mindcloud.matomo.cloud`
- **Official documentation:** [UsersManager create App Specific Token Auth](https://developer.matomo.org/api-reference/reporting-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userLogin` | body | `string` | yes | Matomo API parameter. |
| `passwordConfirmation` | body | `string` | yes | Matomo API parameter. |
| `description` | body | `string` | yes | Matomo API parameter. |
| `expireDate` | body | `string` | no | Matomo API parameter. |
| `expireHours` | body | `string` | no | Matomo API parameter. |
| `secureOnly` | body | `string` | no | Matomo API parameter. |

# UsersManager generate Invite Link with Matomo

## Endpoint

- **Method:** `POST`
- **Path:** `/index.php`
- **Base URL:** `https://mindcloud.matomo.cloud`
- **Official documentation:** [UsersManager generate Invite Link](https://developer.matomo.org/api-reference/reporting-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userLogin` | body | `string` | yes | Matomo API parameter. |
| `expiryInDays` | body | `string` | no | Matomo API parameter. |
| `passwordConfirmation` | body | `string` | no | Matomo API parameter. |

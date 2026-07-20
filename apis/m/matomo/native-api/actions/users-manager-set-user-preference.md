# UsersManager set User Preference with Matomo

## Endpoint

- **Method:** `POST`
- **Path:** `/index.php`
- **Base URL:** `https://mindcloud.matomo.cloud`
- **Official documentation:** [UsersManager set User Preference](https://developer.matomo.org/api-reference/reporting-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userLogin` | body | `string` | yes | Matomo API parameter. |
| `preferenceName` | body | `string` | yes | Matomo API parameter. |
| `preferenceValue` | body | `string` | yes | Matomo API parameter. |

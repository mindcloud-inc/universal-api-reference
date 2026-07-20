# Delete User with OneSignal

Deletes a user from OneSignal.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/apps/:app_id/users/by/:alias_label/:alias_id`
- **Base URL:** `https://api.onesignal.com`
- **Official documentation:** [Delete User](https://documentation.onesignal.com/reference/delete-user)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `alias_id` | path | `string` | yes | The alias value for the selected alias label. |
| `alias_label` | path | `string` | yes | The alias namespace to look up, such as external_id. |

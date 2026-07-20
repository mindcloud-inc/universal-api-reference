# Update User with OneSignal

Updates an existing user in OneSignal.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/apps/:app_id/users/by/:alias_label/:alias_id`
- **Base URL:** `https://api.onesignal.com`
- **Official documentation:** [Update User](https://documentation.onesignal.com/reference/update-user)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `alias_id` | path | `string` | yes | The alias value for the selected alias label. |
| `alias_label` | path | `string` | yes | The alias namespace to look up, such as external_id. |
| `properties` | body | `object` | no | An object of user properties to update. |

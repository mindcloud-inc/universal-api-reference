# Remove Alias with OneSignal

Removes a user alias from OneSignal.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/apps/:app_id/users/by/:alias_label/:alias_id/identity/:alias_label_to_delete`
- **Base URL:** `https://api.onesignal.com`
- **Official documentation:** [Remove Alias](https://documentation.onesignal.com/reference/delete-alias)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `alias_id` | path | `string` | yes | The alias value for the selected alias label. |
| `alias_label` | path | `string` | yes | The alias namespace to look up, such as external_id. |
| `alias_label_to_delete` | path | `string` | yes | The alias namespace to remove from the user. |

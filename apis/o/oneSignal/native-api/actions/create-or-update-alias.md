# Create or Update Alias with OneSignal

Creates or updates a user alias in OneSignal.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/apps/:app_id/users/by/:alias_label/:alias_id/identity`
- **Base URL:** `https://api.onesignal.com`
- **Official documentation:** [Create or Update Alias](https://documentation.onesignal.com/reference/create-alias)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `alias_id` | path | `string` | yes | The alias value for the selected alias label. |
| `alias_label` | path | `string` | yes | The alias namespace to look up, such as external_id. |
| `identity` | body | `object` | yes | An object of aliases to create or update on the user. |

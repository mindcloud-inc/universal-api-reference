# Get User with OneSignal

Retrieves a user from OneSignal by alias.

## Endpoint

- **Method:** `GET`
- **Path:** `/apps/:app_id/users/by/:alias_label/:alias_id`
- **Base URL:** `https://api.onesignal.com`
- **Official documentation:** [Get User](https://documentation.onesignal.com/reference/view-user)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `alias_id` | path | `string` | yes | The alias value for the user to fetch. |
| `alias_label` | path | `string` | yes | The alias type to look up, such as external_id. |

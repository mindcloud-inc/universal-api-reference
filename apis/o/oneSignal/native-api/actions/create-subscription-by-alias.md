# Create Subscription by Alias with OneSignal

Creates a subscription in OneSignal by alias.

## Endpoint

- **Method:** `POST`
- **Path:** `/apps/:app_id/users/by/:alias_label/:alias_id/subscriptions`
- **Base URL:** `https://api.onesignal.com`
- **Official documentation:** [Create Subscription by Alias](https://documentation.onesignal.com/reference/create-subscription)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `alias_id` | path | `string` | yes | The alias value for the selected alias label. |
| `alias_label` | path | `string` | yes | The alias namespace to look up, such as external_id. |
| `subscription` | body | `object` | yes | The subscription object to create for the user. |

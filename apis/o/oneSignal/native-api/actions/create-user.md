# Create User with OneSignal

Creates a user in OneSignal.

## Endpoint

- **Method:** `POST`
- **Path:** `/apps/:app_id/users`
- **Base URL:** `https://api.onesignal.com`
- **Official documentation:** [Create User](https://documentation.onesignal.com/reference/create-user)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identity` | body | `object` | yes | An object of user aliases, such as {"external_id":"user-123"}. |
| `subscriptions[]` | body | `array<object>` | yes | An array of subscription objects to attach to the user. |

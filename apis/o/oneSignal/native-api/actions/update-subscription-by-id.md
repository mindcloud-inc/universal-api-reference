# Update Subscription by ID with OneSignal

Updates a subscription in OneSignal by ID.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/apps/:app_id/subscriptions/:subscription_id`
- **Base URL:** `https://api.onesignal.com`
- **Official documentation:** [Update Subscription by ID](https://documentation.onesignal.com/reference/update-subscription)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subscription` | body | `object` | yes | The subscription fields to update. |
| `subscription_id` | path | `string` | yes | The identifier of the subscription in UUID v4 format. |

# Delete Subscription with OneSignal

Deletes a subscription from OneSignal.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/apps/:app_id/subscriptions/:subscription_id`
- **Base URL:** `https://api.onesignal.com`
- **Official documentation:** [Delete Subscription](https://documentation.onesignal.com/reference/delete-subscription)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subscription_id` | path | `string` | yes | The identifier of the subscription in UUID v4 format. |

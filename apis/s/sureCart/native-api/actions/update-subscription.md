# Update Subscription with SureCart

## Endpoint

- **Method:** `PATCH`
- **Path:** `v1/subscriptions/:id`
- **Base URL:** `https://api.surecart.com`
- **Official documentation:** [Update Subscription](https://developer.surecart.com/api-reference/subscriptions/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The subscription ID to update. |
| `subscription.quantity` | body | `number` | yes | The updated quantity for the subscription. |
| `update_behavior` | query | `string` | no | Optional update timing strategy: immediate or pending. |

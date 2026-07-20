# Cancel/Pause Subscription with SureCart

## Endpoint

- **Method:** `PATCH`
- **Path:** `v1/subscriptions/:id/cancel`
- **Base URL:** `https://api.surecart.com`
- **Official documentation:** [Cancel/Pause Subscription](https://developer.surecart.com/api-reference/subscriptions/cancelpause)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The subscription ID to cancel or pause. |
| `cancel_behavior` | query | `string` | no | Optional cancellation strategy: immediate or pending. |
| `subscription.cancellation_act.comment` | body | `string` | no | Optional cancellation comment. |

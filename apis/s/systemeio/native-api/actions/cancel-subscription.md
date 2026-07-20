# Cancel Subscription with Systeme.io

Cancels an existing subscription in Systeme.io.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/payment/subscriptions/:id/cancel`
- **Base URL:** `https://api.systeme.io`
- **Official documentation:** [Cancel Subscription](https://developer.systeme.io/reference/cancel_subscription-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Subscription identifier. |
| `cancel` | body | `string` | yes | Cancellation timing: Now or WhenBillingPeriodEnds. |

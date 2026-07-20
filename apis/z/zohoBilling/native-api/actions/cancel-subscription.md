# Cancel Subscription with Zoho Billing

## Endpoint

- **Method:** `POST`
- **Path:** `/subscriptions/:subscription_id/cancel`
- **Base URL:** `{api_domain}/billing/v1`
- **Official documentation:** [Cancel Subscription](https://www.zoho.com/billing/api/v1/subscription/#cancel-a-subscription)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subscription_id` | path | `string` | yes | Unique identifier of the subscription. |
| `cancel_at_end` | query | `boolean` | no | When true, Zoho changes the subscription to `non_renewing` instead of cancelling it immediately. |

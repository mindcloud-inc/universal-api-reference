# Cancel Subscription with Stripe

Cancels an existing subscription in Stripe.

## Endpoint

- **Method:** `DELETE`
- **Path:** `subscriptions/:subscription_exposed_id`
- **Base URL:** `https://api.stripe.com/v1`
- **Official documentation:** [Cancel Subscription](https://docs.stripe.com/api/subscriptions/cancel)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subscription_exposed_id` | path | `string` | yes | Subscription identifier. |
| `invoice_now` | body | `boolean` | no | Generate a final invoice now. |
| `prorate` | body | `boolean` | no | Apply prorations on cancellation. |
| `cancellation_details.comment` | body | `string` | no | Optional free-text cancellation comment. |
| `cancellation_details.feedback` | body | `list<string>` | no | Structured cancellation feedback enum. Accepted values: `customer_service`, `low_quality`, `missing_features`, `other`, `switched_service`, `too_complex`, `too_expensive`, `unused`. |
| `expand` | body | `list<string>` | no | Fields to expand in the response. |

# Update Subscription with Stripe

Updates an existing subscription in Stripe.

## Endpoint

- **Method:** `POST`
- **Path:** `subscriptions/:subscription_exposed_id`
- **Base URL:** `https://api.stripe.com/v1`
- **Official documentation:** [Update Subscription](https://docs.stripe.com/api/subscriptions/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subscription_exposed_id` | path | `string` | yes | Subscription identifier. |
| `items.0.id` | body | `string` | no | Existing subscription item ID. |
| `items.0.price` | body | `string` | no | Replacement price for item. |
| `items.0.quantity` | body | `number` | no | Updated quantity for item. |
| `default_payment_method` | body | `string` | no | Default payment method for this subscription. |
| `cancel_at_period_end` | body | `boolean` | no | Whether to cancel at current period end. |
| `proration_behavior` | body | `list<string>` | no | How prorations are handled for updates. Accepted values: `always_invoice`, `create_prorations`, `none`. |
| `payment_behavior` | body | `list<string>` | no | How Stripe handles payment changes. Accepted values: `allow_incomplete`, `default_incomplete`, `error_if_incomplete`, `pending_if_incomplete`. |
| `trial_end` | body | `string` | no | Trial end timestamp or now. |
| `metadata` | body | `object` | no | Metadata key-value pairs. |
| `expand` | body | `list<string>` | no | Fields to expand in the response. |

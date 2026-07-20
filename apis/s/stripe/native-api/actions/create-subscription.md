# Create Subscription with Stripe

Creates a new subscription in Stripe.

## Endpoint

- **Method:** `POST`
- **Path:** `subscriptions`
- **Base URL:** `https://api.stripe.com/v1`
- **Official documentation:** [Create Subscription](https://docs.stripe.com/api/subscriptions/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer` | body | `string` | yes | Identifier of the customer to subscribe. |
| `items.0.price` | body | `string` | no | Price ID for each subscription item. |
| `items.0.quantity` | body | `number` | no | Quantity for each subscription item. |
| `default_payment_method` | body | `string` | no | Payment method attached to invoices for this subscription. |
| `payment_behavior` | body | `list<string>` | no | How Stripe handles the first invoice payment. Accepted values: `allow_incomplete`, `default_incomplete`, `error_if_incomplete`. |
| `collection_method` | body | `list<string>` | no | How to collect payment for this subscription. Accepted values: `charge_automatically`, `send_invoice`. |
| `trial_end` | body | `string` | no | Trial end timestamp or now. |
| `metadata` | body | `object` | no | Metadata key-value pairs for the subscription. |
| `expand` | body | `list<string>` | no | Fields to expand in the response. |

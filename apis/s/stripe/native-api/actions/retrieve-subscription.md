# Retrieve Subscription with Stripe

Retrieves a subscription from your Stripe account.

## Endpoint

- **Method:** `GET`
- **Path:** `subscriptions/:subscription_exposed_id`
- **Base URL:** `https://api.stripe.com/v1`
- **Official documentation:** [Retrieve Subscription](https://docs.stripe.com/api/subscriptions/retrieve)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subscription_exposed_id` | path | `string` | yes | Subscription identifier. |
| `expand` | query | `list<string>` | no | Fields to expand in the response. |

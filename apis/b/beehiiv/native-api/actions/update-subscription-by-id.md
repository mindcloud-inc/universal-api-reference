# Update Subscription by ID with Beehiiv

Updates a subscription in Beehiiv by ID.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v2/publications/:publicationId/subscriptions/:subscriptionId`
- **Base URL:** `https://api.beehiiv.com`
- **Official documentation:** [Update Subscription by ID](https://developers.beehiiv.com/api-reference/subscriptions/patch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `publicationId` | path | `string` | yes | The prefixed ID of the publication object. |
| `subscriptionId` | path | `string` | yes | The prefixed ID of the subscription object. |
| `email` | body | `string` | no | Optional new email address for the subscription. |
| `unsubscribe` | body | `boolean` | no | Set true to unsubscribe the subscription. |
| `tier` | body | `string` | no | Optional tier update value. |
| `stripe_customer_id` | body | `string` | no | Optional Stripe customer identifier. |

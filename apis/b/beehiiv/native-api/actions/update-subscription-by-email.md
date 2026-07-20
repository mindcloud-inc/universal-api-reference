# Update Subscription by Email with Beehiiv

Updates a subscription in Beehiiv by email address.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v2/publications/:publicationId/subscriptions/by_email/:email`
- **Base URL:** `https://api.beehiiv.com`
- **Official documentation:** [Update Subscription by Email](https://developers.beehiiv.com/api-reference/subscriptions/update-by-email)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `publicationId` | path | `string` | yes | The prefixed ID of the publication object. |
| `email` | path | `string` | yes | Email address (URL-encoded in path). |
| `email` | body | `string` | no | Optional new email address for the subscription. |
| `unsubscribe` | body | `boolean` | no | Set true to unsubscribe the subscription. |
| `tier` | body | `string` | no | Optional tier update value. |
| `stripe_customer_id` | body | `string` | no | Optional Stripe customer identifier. |

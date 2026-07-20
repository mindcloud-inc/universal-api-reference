# Create Interest Subscription with Flexmail

Creates an interest subscription for a contact in Flexmail.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts/{id}/interest-subscriptions`
- **Base URL:** `https://api.flexmail.eu`
- **Official documentation:** [Create Interest Subscription](https://api.flexmail.eu/documentation/#post-/contacts/-id-/interest-subscriptions)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `number` | yes |
| `interest_id` | body | `string` | yes |

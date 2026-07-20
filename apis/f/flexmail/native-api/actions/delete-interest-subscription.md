# Delete Interest Subscription with Flexmail

Deletes an interest subscription from a contact in Flexmail.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/contacts/{id}/interest-subscriptions/{interest_id}`
- **Base URL:** `https://api.flexmail.eu`
- **Official documentation:** [Delete Interest Subscription](https://api.flexmail.eu/documentation/#delete-/contacts/-id-/interest-subscriptions/-interest_id-)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `number` | yes |
| `interest_id` | path | `string` | yes |

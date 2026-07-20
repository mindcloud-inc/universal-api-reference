# Update Subscription with Pinghome

Updates an existing subscription in Pinghome.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/payment-cmd/v1/subscription/:id`
- **Base URL:** `https://api.pinghome.io`
- **Official documentation:** [Update Subscription](https://docs.pinghome.io/billing-operations-management/update-subscription/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | no | The subscription ID to update. |
| `price_id` | body | `string` | no | The target price ID for the updated subscription. |

# Update Subscription with Pabbly Subscription Billing

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/subscription/:subscriptionId/update`
- **Base URL:** `https://payments.pabbly.com/api`
- **Official documentation:** [Update Subscription](https://apidocs.pabbly.com/#7f183e52-2085-4f9b-8abd-26ba39fe12d8)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `custom_fields` | body | `string` | no | — |
| `method_id` | body | `string` | no | — |
| `payment_mode` | body | `string` | no | — |
| `subscription_id` | path | `string` | no | Pabbly Subscription ID. |
| `update_reason` | body | `string` | no | — |

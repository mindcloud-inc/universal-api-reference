# Cancel Subscription For Existing Customer with Pabbly Subscription Billing

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/subscription/:subscriptionId/cancel`
- **Base URL:** `https://payments.pabbly.com/api`
- **Official documentation:** [Cancel Subscription For Existing Customer](https://apidocs.pabbly.com/#86de662e-d6ef-4a8b-a35f-a37c8b2f880e)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cancel_at_end` | body | `string` | no | True to cancel at the end of subscription, false to cancel immediately. |
| `subscription_id` | path | `string` | no | Pabbly Subscription ID. |

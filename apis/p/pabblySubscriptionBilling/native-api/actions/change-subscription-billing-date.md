# Change Subscription Billing Date with Pabbly Subscription Billing

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/subscription/change-billing/:subscriptionId`
- **Base URL:** `https://payments.pabbly.com/api`
- **Official documentation:** [Change Subscription Billing Date](https://apidocs.pabbly.com/#37492ea6-99bc-4b8e-81eb-8c7165a86eca)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `change_reason` | body | `string` | no |
| `next_billing_date` | body | `string` | no |
| `subscription_id` | path | `string` | no |

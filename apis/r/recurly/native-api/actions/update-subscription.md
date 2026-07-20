# Update Subscription with Recurly

## Endpoint

- **Method:** `PUT`
- **Path:** `/subscriptions/:subscription_id`
- **Base URL:** `https://v3.recurly.com`
- **Official documentation:** [Update Subscription](https://recurly.com/developers/api/v2021-02-25/#operation/update_subscription)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `auto_renew` | body | `boolean` | no | — |
| `collection_method` | body | `string` | no | Accepted values: `0`, `1`. |
| `customer_notes` | body | `string` | no | — |
| `net_terms` | body | `number` | no | — |
| `next_bill_date` | body | `date` | no | — |
| `po_number` | body | `string` | no | — |
| `remaining_billing_cycles` | body | `number` | no | — |
| `renewal_billing_cycles` | body | `number` | no | — |
| `subscription_id` | path | `string` | yes | — |
| `terms_and_conditions` | body | `string` | no | — |

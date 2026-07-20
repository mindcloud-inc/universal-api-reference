# Create Subscription with Recurly

## Endpoint

- **Method:** `POST`
- **Path:** `/subscriptions`
- **Base URL:** `https://v3.recurly.com`
- **Official documentation:** [Create Subscription](https://recurly.com/developers/api/v2021-02-25/#operation/create_subscription)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account.code` | body | `string` | yes | — |
| `auto_renew` | body | `boolean` | no | — |
| `collection_method` | body | `string` | no | Accepted values: `0`, `1`. |
| `currency` | body | `string` | yes | — |
| `customer_notes` | body | `string` | no | — |
| `plan_code` | body | `string` | yes | — |
| `po_number` | body | `string` | no | — |
| `quantity` | body | `number` | no | — |
| `unit_amount` | body | `number` | no | — |

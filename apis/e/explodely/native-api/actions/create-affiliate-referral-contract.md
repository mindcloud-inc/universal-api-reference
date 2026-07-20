# Create Affiliate Referral Contract with Explodely

Creates a new affiliate referral contract in Explodely.

## Endpoint

- **Method:** `POST`
- **Path:** `/aff`
- **Base URL:** `https://explodely.com/api/v1`
- **Official documentation:** [Create Affiliate Referral Contract](https://docs.explodely.com/api/create-affiliate-referral-contract)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contract_name` | body | `string` | yes | A name for the contract in your seller records. |
| `partner_username` | body | `string` | yes | The Explodely affiliate ID of the partner. |
| `product` | body | `string` | yes | The Explodely product ID or allproducts. |
| `commission` | body | `string` | yes | The percentage of your share the partner will get, up to 80. |
| `start_date` | body | `string` | no | Optional start date in dd-mmm-yyyy format. |
| `end_date` | body | `string` | no | Optional end date in dd-mmm-yyyy format. |
| `max_earnings` | body | `string` | no | Optional contract earnings cap. |
| `max_sales` | body | `string` | no | Optional contract sales cap. |
| `comments` | body | `string` | no | Optional comments shown in the seller contracts section. |
| `activate` | body | `string` | no | Set to yes to activate the contract immediately. |
| `mutual_termination` | body | `string` | no | Set to yes to require both parties to approve termination. |

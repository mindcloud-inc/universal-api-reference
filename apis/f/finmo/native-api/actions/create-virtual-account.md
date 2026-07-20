# Create Virtual Account with Finmo

Creates a new virtual account in Finmo.

## Endpoint

- **Method:** `POST`
- **Path:** `/virtual-account`
- **Base URL:** `https://api.finmo.net/v1/`
- **Official documentation:** [Create Virtual Account](https://docs.finmo.net/reference/newvirtualaccount-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `currency` | body | `string` | yes | Virtual account currency. |
| `customer_id` | body | `string` | yes | Customer reference for the virtual account. |
| `scope` | body | `string` | no | Virtual account scope. |
| `credit_wallet_id` | body | `string` | no | Wallet ID to credit. Use instead of credit wallet category when known. |
| `credit_wallet_category` | body | `string` | no | Wallet category to credit when a wallet ID is not provided. |
| `fees_wallet_id` | body | `string` | no | Fees wallet ID. |
| `description` | body | `string` | no | Description for the virtual account. |
| `payin_method_name` | body | `string` | yes | Payin method name for the virtual account. |
| `payin_method_param` | body | `object` | no | Additional payin method parameters. |
| `organization_reference_id` | body | `string` | no | Organization reference identifier for the virtual account. |
| `webhook_url` | body | `string` | no | Override webhook URL for this virtual account. |
| `metadata` | body | `object` | no | Custom metadata object. |

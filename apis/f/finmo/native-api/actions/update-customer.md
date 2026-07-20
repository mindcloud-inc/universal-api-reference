# Update Customer with Finmo

Updates an existing customer in Finmo.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/customer/:customer_id`
- **Base URL:** `https://api.finmo.net/v1/`
- **Official documentation:** [Update Customer](https://docs.finmo.net/reference/updatecustomer-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer_id` | path | `string` | yes | Customer identifier to update. |
| `description` | body | `string` | no | Description about the customer. |
| `type` | body | `string` | yes | Customer type: company or individual. |
| `organization_reference_id` | body | `string` | no | Organization reference identifier for the customer. |
| `is_enabled` | body | `boolean` | no | Flag to enable or disable the customer. |
| `metadata` | body | `object` | no | Custom metadata object. |
| `account_usage_purpose` | body | `string` | yes | Purpose of opening the account. |
| `company` | body | `object` | no | Company payload when the customer type is company. |
| `individual` | body | `object` | no | Individual payload when the customer type is individual. |

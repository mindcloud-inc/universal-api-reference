# Create Customer with Finmo

Creates a new customer in Finmo.

## Endpoint

- **Method:** `POST`
- **Path:** `/customer`
- **Base URL:** `https://api.finmo.net/v1/`
- **Official documentation:** [Create Customer](https://docs.finmo.net/reference/newcustomer-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | Description about the customer. |
| `type` | body | `string` | yes | Customer type: company or individual. |
| `organization_reference_id` | body | `string` | no | Organization reference identifier for the customer. |
| `metadata` | body | `object` | no | Custom metadata object. |
| `account_usage_purpose` | body | `string` | yes | Purpose of opening the account. |
| `company` | body | `object` | no | Company payload when the customer type is company. |
| `individual` | body | `object` | no | Individual payload when the customer type is individual. |

# Create a Selling Policy with eBay

Retrieve a specific list of seller policies (i.e. fulfillment, payment & return policies)

## Endpoint

- **Method:** `POST`
- **Path:** `sell/account/v1/:policy`
- **Base URL:** `https://api.ebay.com/`
- **API:** REST
- **Official documentation:** [Create a Selling Policy](https://developer.ebay.com/api-docs/sell/account/resources/custom_policy/methods/getCustomPolicies)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | A seller-defined name for this return business policy. Names must be unique for policies assigned to the same marketplace. |
| `policy` | path | `list<string>` | yes | Specify which type of policies to create. Accepted values are: payment_policy, return_policy, fulfillment_policy, and custom_policy. |
| `marketplaceId` | body | `string` | yes | The eBay marketplace_id to retrieve the specified policies from. |
| `description` | body | `string` | no | A seller-defined description of the return business policy. This description is only for the seller's use, and is not exposed on any eBay pages. |

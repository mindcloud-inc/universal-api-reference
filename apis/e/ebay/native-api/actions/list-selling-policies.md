# List Selling Policies with eBay

Retrieve a specific list of selling policies (i.e. fulfillment, payment & return policies)

## Endpoint

- **Method:** `GET`
- **Path:** `sell/account/v1/:policy/`
- **Base URL:** `https://api.ebay.com/`
- **API:** REST
- **Official documentation:** [List Selling Policies](https://developer.ebay.com/api-docs/sell/account/resources/custom_policy/methods/getCustomPolicies)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `marketplace_id` | query | `string` | yes | The eBay marketplace_id to retrieve the specified policies from. |
| `policy` | path | `list<string>` | yes | Specify which list of policies to retrieve. Accepted values are: payment, return, fulfillment, custom. |
| `policy_types` | query | `string<string>` | no | (optional) parameter to be used only when retrieving "Custom" policies. Omitting this query parameter from a Custom Policies request will return all custom policies of all policy types. |

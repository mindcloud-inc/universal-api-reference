# Update Product with Cryptlex

Updates an existing product in Cryptlex.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v3/products/:id`
- **Base URL:** `https://api.cryptlex.com`
- **Official documentation:** [Update Product](https://api.cryptlex.com/v3/docs#tag/Products/operation/patch/v3/products/%7Bid%7D)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Unique identifier for the product. |
| `name` | body | `string` | no | Unique name for the product. |
| `displayName` | body | `string` | no | Display name for the product. |
| `description` | body | `string` | no | Description for the product. |
| `automatedEmails` | body | `list<string>` | no | Automated emails enabled for the product. |
| `licenseTemplateId` | body | `string` | no | License template linked to the product. |
| `licensePolicyId` | body | `string` | no | License policy linked to the product. |
| `trialPolicyId` | body | `string` | no | Trial policy linked to the product. |

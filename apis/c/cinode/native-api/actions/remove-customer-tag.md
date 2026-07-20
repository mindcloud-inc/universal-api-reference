# Remove Customer Tag with Cinode

Removes a tag from a customer in Cinode.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v0.2/companies/:companyId/customers/:customerId/tags/:tagId`
- **Base URL:** `https://api.cinode.com`
- **Official documentation:** [Remove Customer Tag](https://api.cinode.com/docs/index.html#/CompanyCustomerTags/UntagCustomerV02)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyId` | path | `number` | yes | Cinode company identifier. |
| `customerId` | path | `number` | yes | Identifier of the customer. |
| `tagId` | path | `number` | yes | Identifier of the tag to remove. |

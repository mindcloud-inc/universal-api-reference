# Add Customer Tag with Cinode

Adds a tag to a customer in Cinode.

## Endpoint

- **Method:** `POST`
- **Path:** `/v0.2/companies/:companyId/customers/:customerId/tags`
- **Base URL:** `https://api.cinode.com`
- **Official documentation:** [Add Customer Tag](https://api.cinode.com/docs/index.html#/CompanyCustomerTags/TagCustomerV02)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyId` | path | `number` | yes | Cinode company identifier. |
| `customerId` | path | `number` | yes | Identifier of the customer. |
| `id` | body | `number` | no | Existing tag identifier to add. |
| `name` | body | `string` | no | Tag name to create or match. |

# List Customer Tags with Cinode

Retrieves tags for a customer in Cinode.

## Endpoint

- **Method:** `GET`
- **Path:** `/v0.2/companies/:companyId/customers/:customerId/tags`
- **Base URL:** `https://api.cinode.com`
- **Official documentation:** [List Customer Tags](https://api.cinode.com/docs/index.html#/CompanyCustomerTags/GetCustomerTagsV02)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyId` | path | `number` | yes | Cinode company identifier. |
| `customerId` | path | `number` | yes | Identifier of the customer. |

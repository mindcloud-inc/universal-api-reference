# Get Customer with Cinode

Retrieves a customer from Cinode.

## Endpoint

- **Method:** `GET`
- **Path:** `/v0.1/companies/:companyId/customers/:id`
- **Base URL:** `https://api.cinode.com`
- **Official documentation:** [Get Customer](https://api.cinode.com/docs/index.html#/CompanyCustomer/GetCompanyCustomer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyId` | path | `number` | yes | Cinode company ID. |
| `id` | path | `number` | yes | Customer ID. |

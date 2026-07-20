# List Customers with Cinode

Retrieves a company customer list from Cinode.

## Endpoint

- **Method:** `GET`
- **Path:** `/v0.1/companies/:companyId/customers`
- **Base URL:** `https://api.cinode.com`
- **Official documentation:** [List Customers](https://api.cinode.com/docs/index.html#/CompanyCustomers/CompanyCustomers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyId` | path | `number` | yes | Cinode company ID. |

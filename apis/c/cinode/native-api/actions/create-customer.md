# Create Customer with Cinode

Creates a new customer in Cinode.

## Endpoint

- **Method:** `POST`
- **Path:** `/v0.1/companies/:companyId/customers`
- **Base URL:** `https://api.cinode.com`
- **Official documentation:** [Create Customer](https://api.cinode.com/docs/index.html#/CompanyCustomer/NewCompanyCustomer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyId` | path | `number` | yes | Cinode company ID. |
| `name` | body | `string` | yes | Customer name. |
| `description` | body | `string` | no | Customer description. |
| `corporateIdentityNumber` | body | `string` | no | Customer corporate identity number. |
| `intermediator` | body | `boolean` | no | Whether the customer is an intermediary. |
| `size` | body | `number` | no | Company size enum. 0=Self employed, 1=2-10, 2=11-50, 3=51-200, 4=201-500, 5=501-1,000, 6=1,001-5,000, 7=5,001-10,000, 8=10,001+. |
| `turnOver` | body | `number` | no | Customer turnover. |
| `turnOverCurrencyId` | body | `number` | no | Currency ID for turnover. |

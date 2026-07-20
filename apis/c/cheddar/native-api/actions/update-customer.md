# Update Customer with Cheddar

Updates existing customer details in Cheddar.

## Endpoint

- **Method:** `POST`
- **Path:** `/customers/edit-customer/productCode/{productCode}/code/:customerCode`
- **Base URL:** `https://getcheddar.com/xml`
- **Official documentation:** [Update Customer](https://docs.getcheddar.com/#update-a-customer-only)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | path | `string` | yes | Customer code from Cheddar. |
| `firstName` | body | `string` | no | Customer first name. |
| `lastName` | body | `string` | no | Customer last name. |
| `email` | body | `string` | no | Customer email address. |
| `company` | body | `string` | no | Customer company name. |
| `notes` | body | `string` | no | Internal notes for the customer. |
| `remoteAddress` | body | `string` | no | Client IPv4 address for fraud protection and rate limiting. |

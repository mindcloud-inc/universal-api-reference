# Get Customer with MILKEE

Retrieves a customer from MILKEE.

## Endpoint

- **Method:** `GET`
- **Path:** `/companies/:companyId/customers/:customerId`
- **Base URL:** `https://app.milkee.ch/api/v2`
- **Official documentation:** [Get Customer](https://apidocs.milkee.ch/api/resources/customers.html#einzelnen-customer-abrufen)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company` | path | `string` | yes | The numeric MILKEE company ID used in the request path. |
| `customer` | path | `string` | yes | The numeric MILKEE customer ID used in the request path. |

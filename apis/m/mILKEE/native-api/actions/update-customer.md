# Update Customer with MILKEE

Updates an existing customer in MILKEE.

## Endpoint

- **Method:** `PUT`
- **Path:** `/companies/:companyId/customers/:customerId`
- **Base URL:** `https://app.milkee.ch/api/v2`
- **Official documentation:** [Update Customer](https://apidocs.milkee.ch/api/resources/customers.html#customer-aktualisieren)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `archived` | body | `boolean` | no | Archive the customer when true. |
| `company` | path | `string` | yes | The numeric MILKEE company ID used in the request path. |
| `customer` | path | `string` | yes | The numeric MILKEE customer ID used in the request path. |
| `default_hourly_rate` | body | `number` | no | Default hourly rate in CHF. |
| `email` | body | `string` | no | Customer email address. |
| `name` | body | `string` | no | Customer company name. |
| `tax_rate_id` | body | `number` | no | Associated tax rate ID. |

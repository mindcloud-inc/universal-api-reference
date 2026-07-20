# Create Customer with MILKEE

Creates a new customer in MILKEE.

## Endpoint

- **Method:** `POST`
- **Path:** `/companies/:companyId/customers`
- **Base URL:** `https://app.milkee.ch/api/v2`
- **Official documentation:** [Create Customer](https://apidocs.milkee.ch/api/resources/customers.html#neuen-customer-erstellen)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `city` | body | `string` | no | City name. |
| `company` | path | `string` | yes | The numeric MILKEE company ID used in the request path. |
| `contact_name` | body | `string` | no | Primary contact name. MILKEE creates a main contact automatically when this is provided. |
| `default_hourly_rate` | body | `number` | no | Default hourly rate in CHF. |
| `email` | body | `string` | no | Customer email address. |
| `name` | body | `string` | yes | Customer company name. |
| `street` | body | `string` | no | Street address. |
| `tax_rate_id` | body | `number` | no | Associated tax rate ID. |
| `zip` | body | `string` | no | Postal code. |

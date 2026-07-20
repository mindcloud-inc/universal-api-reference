# List Customer Attributes with Customer.io

Retrieves attributes for a customer in Customer.io.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/customers/:customer_id/attributes`
- **Base URL:** `https://api.customer.io`
- **Official documentation:** [List Customer Attributes](https://docs.customer.io/integrations/api/app/#tag/Customers/operation/getPersonAttributes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer_id` | path | `string` | yes | The ID of the customer to inspect. |
| `id_type` | query | `list<string>` | no | The type of identifier provided in Customer ID. Accepted values: `cio_id`, `email`, `id`. |

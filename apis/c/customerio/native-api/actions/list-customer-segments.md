# List Customer Segments with Customer.io

Retrieves segments for a customer in Customer.io.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/customers/:customer_id/segments`
- **Base URL:** `https://api.customer.io`
- **Official documentation:** [List Customer Segments](https://docs.customer.io/integrations/api/app/#tag/Customers/operation/getPersonSegments)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer_id` | path | `string` | yes | The ID of the customer to inspect. |
| `id_type` | query | `list<string>` | no | The type of identifier provided in Customer ID. Accepted values: `cio_id`, `email`, `id`. |

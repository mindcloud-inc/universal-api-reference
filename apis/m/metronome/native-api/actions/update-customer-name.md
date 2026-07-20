# Update Customer Name with Metronome

Updates a customer name in Metronome.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/customers/:customer_id/setName`
- **Base URL:** `https://api.metronome.com`
- **Official documentation:** [Update Customer Name](https://docs.metronome.com/api-reference/customers/update-a-customer-name)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer_id` | path | `string` | yes | The customer ID. |
| `name` | body | `string` | yes | The new customer name. |

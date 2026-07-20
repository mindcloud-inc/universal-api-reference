# Get Customer with Housecall Pro

## Endpoint

- **Method:** `GET`
- **Path:** `/customers/:customer_id`
- **Base URL:** `https://api.housecallpro.com`
- **Official documentation:** [Get Customer](https://docs.housecallpro.com/docs/housecall-public-api/7599b1ec89338-get-customer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer_id` | path | `string` | yes | ID of the customer to retrieve. |
| `expand[]` | query | `array<string>` | no | Fields to expand in the response body. Send multiple values as a array. |

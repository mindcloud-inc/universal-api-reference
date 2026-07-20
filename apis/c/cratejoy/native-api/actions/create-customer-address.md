# Create Customer Address with Cratejoy

Creates a customer address in Cratejoy.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/customers/:customerId/addresses/`
- **Base URL:** `https://api.cratejoy.com`
- **Official documentation:** [Create Customer Address](https://docs.cratejoy.com/reference/methods-customer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `number` | yes | The Cratejoy customer ID. |
| `to` | body | `string` | no | The name on the address. |
| `street` | body | `string` | no | The street line for the address. |
| `city` | body | `string` | no | The city for the address. |
| `state` | body | `string` | no | The state or province for the address. |
| `zip_code` | body | `string` | no | The postal code for the address. |
| `country` | body | `string` | no | The two-letter country code for the address. |

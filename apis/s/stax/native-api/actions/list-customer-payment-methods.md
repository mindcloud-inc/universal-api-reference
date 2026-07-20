# List Customer Payment Methods with Stax

Retrieves a customer's payment methods from Stax.

## Endpoint

- **Method:** `GET`
- **Path:** `/customer/:customerId/payment-method`
- **Base URL:** `https://apiprod.fattlabs.com`
- **Official documentation:** [List Customer Payment Methods](https://docs.staxpayments.com/reference/get-all-payment-methods-for-a-customer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `string` | no | Customer identifier |

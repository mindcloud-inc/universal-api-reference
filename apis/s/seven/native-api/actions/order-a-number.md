# Order a Number with Seven

Creates a new number order in Seven.

## Endpoint

- **Method:** `POST`
- **Path:** `/numbers/order`
- **Base URL:** `https://gateway.seven.io/api`
- **Official documentation:** [Order a Number](https://docs.seven.io/en/rest-api/endpoints/numbers#order-a-number)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `number` | body | `string` | yes | The phone number to order. |
| `payment_interval` | body | `string` | no | The payment interval for the number. Possible values are monthly and annually (default). |

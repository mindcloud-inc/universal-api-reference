# Get Abandoned Cart with Big Cartel

Retrieves an abandoned cart from Big Cartel.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/accounts/[:account-id]/carts/[:cart-id]`
- **Base URL:** `https://api.bigcartel.com`
- **Official documentation:** [Get Abandoned Cart](https://developers.bigcartel.com/api/v1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account-id` | path | `number` | yes | The Big Cartel account ID. |
| `cart-id` | path | `string` | yes | The Big Cartel cart ID. |

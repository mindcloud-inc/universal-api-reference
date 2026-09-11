# Get Cart v2 with BigCommerce

## Endpoint

- **Method:** `GET`
- **URL:** `https://api.bigcommerce.com/stores/:storeHash/v3/carts/:cartId`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cartId` | path | `string` | yes | — |
| `include` | query | `string` | no | what to include in the response |
| `storeHash` | path | `string` | no | — |

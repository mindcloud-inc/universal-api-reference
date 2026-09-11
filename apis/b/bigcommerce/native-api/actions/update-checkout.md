# Update Checkout with BigCommerce

## Endpoint

- **Method:** `PUT`
- **Path:** `/v3/checkouts/:cartID`
- **Base URL:** `https://api.bigcommerce.com/stores/{storeHash}`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cartID` | path | `string` | yes | — |
| `customer_message` | body | `string` | yes | Maximum length: 2000. |

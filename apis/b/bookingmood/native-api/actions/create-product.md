# Create Product with Bookingmood

Creates a new product in the Bookingmood API.

## Endpoint

- **Method:** `POST`
- **Path:** `/products`
- **Base URL:** `https://api.bookingmood.com/v1`
- **Official documentation:** [Create Product](https://www.bookingmood.com/en-US/api-reference/products)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name.default` | body | `string` | yes | Localized product name. |
| `rent_period` | body | `string` | yes | Rent period for the product. |
| `timezone` | body | `string` | yes | Timezone for the product. |

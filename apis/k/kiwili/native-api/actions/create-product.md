# Create Product with Kiwili

Creates a new product in Kiwili.

## Endpoint

- **Method:** `POST`
- **Path:** `/product`
- **Base URL:** `https://mindcloud.kiwili.com/api`
- **Official documentation:** [Create Product](https://api.kiwili.com/api/openapi/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Active` | body | `boolean` | no | Whether the product is active. |
| `Name` | body | `string` | yes | The product name. |
| `Price` | body | `number` | yes | The product price. |

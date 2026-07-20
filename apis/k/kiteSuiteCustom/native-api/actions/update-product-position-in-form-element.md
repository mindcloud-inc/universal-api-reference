# Update Product Position in Form Element with Kite Suite

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v1/form/element/product/position/:id`
- **Base URL:** `https://api.kitesuite.com`
- **Official documentation:** [Update Product Position in Form Element](https://api.kitesuite.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | yes | Request body |
| `id` | path | `string` | yes | ID of the form element. |
| `productId` | body | `string` | yes | ID of the product to reposition. |
| `newPosition` | body | `number` | yes | New position of the product in the myProducts array. |

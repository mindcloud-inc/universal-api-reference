# Update Category with Voucherify

Updates an existing category in Voucherify.

## Endpoint

- **Method:** `PUT`
- **Path:** `/categories/:categoryId`
- **Base URL:** `https://us1.api.voucherify.io/v1`
- **Official documentation:** [Update Category](https://docs.voucherify.io/api-reference/categories)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `categoryId` | path | `string` | yes |
| `hierarchy` | body | `number` | yes |
| `name` | body | `string` | yes |

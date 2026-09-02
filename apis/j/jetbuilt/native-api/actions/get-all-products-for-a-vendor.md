# Get All Products for a Vendor with Jetbuilt

Retrieves all products with your connected pricing for a specified vendor.

## Endpoint

- **Method:** `GET`
- **Path:** `product_databases/:dbid/vendors/:vendor/products`
- **Base URL:** `https://app.jetbuilt.com/api/`
- **Official documentation:** [Get All Products for a Vendor](https://api.jetbuilt.com/customers?shell--json#get-all-products-for-a-vendor)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dbid` | path | `string` | no | The ID of the product database. |
| `vendor` | path | `string` | no | The ID of the vendor (An approved Manufacturer or Distributor) |

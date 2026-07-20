# Get Warehouse Delivery Options with TikTok Shop

This API is used to obtain a list of delivery options available through the seller's designated warehouse.

## Endpoint

- **Method:** `GET`
- **Path:** `logistics/202309/warehouses/:warehouse_id/delivery_options`
- **Base URL:** `https://open-api.tiktokglobalshop.com/`
- **Official documentation:** [Get Warehouse Delivery Options](https://partner.tiktokshop.com/docv2/page/get-warehouse-delivery-options-202309)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `warehouse_id` | path | `string` | no |
| `shop_cipher` | query | `list<string>` | no |

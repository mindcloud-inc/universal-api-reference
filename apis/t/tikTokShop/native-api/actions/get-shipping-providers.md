# Get Shipping Providers with TikTok Shop

This API is used to obtain the shipping provider corresponding to the specified delivery option.

## Endpoint

- **Method:** `GET`
- **Path:** `logistics/202309/delivery_options/:delivery_option_id/shipping_providers`
- **Base URL:** `https://open-api.tiktokglobalshop.com/`
- **Official documentation:** [Get Shipping Providers](https://partner.tiktokshop.com/docv2/page/get-shipping-providers-202309)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `delivery_option_id` | path | `string` | yes |
| `shop_cipher` | query | `list<string>` | yes |

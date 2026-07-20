# Get Product with TikTok Shop

Retrieve all properties of a product that is in the DRAFT, PENDING, or ACTIVATE status.

## Endpoint

- **Method:** `GET`
- **Path:** `product/202309/products/:product_id`
- **Base URL:** `https://open-api.tiktokglobalshop.com/`
- **Official documentation:** [Get Product](https://partner.tiktokshop.com/docv2/page/get-product-202309)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `shop_cipher` | query | `list<string>` | no | Use this property to pass shop information in requesting the API. Failure in passing the correct value when requesting the API for cross-border shops will return incorrect response.  Get by API Get Authorization Shop |
| `return_under_review_version` | query | `string` | no | A flag to indicate what product information to retrieve if a live product (ACTIVATE status) is edited and resent for TikTok Shop review. - True: Retrieves the latest version of the product information that is currently under review. - False: Retrieves a snapshot of the product information that is live and online (before the edit). Default: False |
| `product_id` | path | `string` | no | — |

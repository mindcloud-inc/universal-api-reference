# Get Package Shipping Document (v2) with TikTok Shop

## Endpoint

- **Method:** `GET`
- **Path:** `/fulfillment/202309/packages/:package_id/shipping_documents`
- **Base URL:** `https://open-api.tiktokglobalshop.com/`
- **Official documentation:** [Get Package Shipping Document (v2)](https://partner.tiktokshop.com/docv2/page/6507ead7b99d5302be949ba9?external_id=6507ead7b99d5302be949ba9)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `shop_cipher` | query | `list<list>` | no |
| `document_type` | query | `string` | yes |
| `document_size` | query | `string` | no |
| `document_format` | query | `string` | no |
| `package_id` | path | `string` | yes |

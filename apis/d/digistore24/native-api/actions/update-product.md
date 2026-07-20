# Update Product with Digistore24

Updates an existing product in Digistore24.

## Endpoint

- **Method:** `PUT`
- **Path:** `/updateProduct`
- **Base URL:** `https://www.digistore24.com/api/call`
- **Official documentation:** [Update Product](https://digistore24.com/api/docs/paths/updateProduct.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `product_id` | query | `number` | yes | Product ID |
| `name_de` | body | `string` | no | Product name in German |
| `name_en` | body | `string` | no | Product name in English |
| `name_es` | body | `string` | no | Product name in Spanish |
| `name_intern` | body | `string` | no | Internal product name |
| `description_de` | body | `string` | no | Product description in German |
| `description_en` | body | `string` | no | Product description in English |
| `description_es` | body | `string` | no | Product description in Spanish |
| `salespage_url` | body | `string` | no | Sales page URL |
| `upsell_salespage_url` | body | `string` | no | Upsell sales page URL |
| `thankyou_url` | body | `string` | no | Thank you page URL |
| `image_url` | body | `string` | no | Product image URL |
| `product_type_id` | body | `number` | no | Product type ID |
| `currency` | body | `string` | no | Currencies for payments |
| `approval_status` | body | `string` | no | Approval status |
| `affiliate_commision` | body | `number` | no | Commission for affiliates |
| `buyer_type` | body | `string` | no | Buyer type |
| `is_address_input_mandatory` | body | `boolean` | no | Whether buyer address input is mandatory |
| `add_order_data_to_thankyou_page_url` | body | `boolean` | no | Whether order data is added to the thank you URL |

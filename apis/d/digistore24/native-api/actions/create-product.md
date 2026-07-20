# Create Product with Digistore24

Creates a new product in Digistore24.

## Endpoint

- **Method:** `POST`
- **Path:** `/createProduct`
- **Base URL:** `https://www.digistore24.com/api/call`
- **Official documentation:** [Create Product](https://digistore24.com/api/docs/paths/createProduct.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data` | query | `object` | yes | Product properties object |
| `data.name_intern` | query | `string` | no | Internal product name |
| `data.name_de` | query | `string` | no | German product name |
| `data.name_en` | query | `string` | no | English product name |
| `data.name_es` | query | `string` | no | Spanish product name |
| `data.description_de` | query | `string` | no | German product description |
| `data.description_en` | query | `string` | no | English product description |
| `data.description_es` | query | `string` | no | Spanish product description |
| `data.salespage_url` | query | `string` | no | Sales page URL |
| `data.upsell_salespage_url` | query | `string` | no | Upsell sales page URL |
| `data.thankyou_url` | query | `string` | no | Thank you page URL |
| `data.image_url` | query | `string` | no | Product image URL |
| `data.product_type_id` | query | `number` | no | Product type ID |
| `data.approval_status` | query | `string` | no | Product approval status |
| `data.affiliate_commission` | query | `number` | no | Affiliate commission amount |
| `data.buyer_type` | query | `string` | no | Buyer type |
| `data.is_address_input_mandatory` | query | `string` | no | Whether address input is mandatory |
| `data.add_order_data_to_thankyou_page_url` | query | `string` | no | Whether to append order data to the thank you URL |

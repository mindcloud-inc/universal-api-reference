# <img src="https://images.mindcloud.co/apps/icons/image-2820-vectorized_1776860358018.png" alt="Rithum for Brands logo" width="28" height="28"> Rithum for Brands: Universal API

Rithum for Brands was formerly know as ChannelAdvisor. Connect with more consumers by streamlining operations, expanding to new channels and growing sales from a centralized platform.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/rithumForBrands/latest
- **Category:** Commerce
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.rithum.com/
- **Vendor API docs:** https://knowledge.channeladvisor.com/kc?id=kb_category_main&kb_knowledge_base=fdc1945887cf4910b535a7183cbb35bd

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Profiles](actions/list-profiles.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rithumForBrands/latest/actions/list-profiles?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Fulfillment

| Action | Method | Description |
| --- | --- | --- |
| [Get Order Fulfillments](actions/get-order-fulfillments.md) | GET | Retrieve all fulfillments for a specified order. |
| [List Fulfillments](actions/list-fulfillments.md) | GET | Retrieve existing Fulfillments. |

### Inventories

| Action | Method | Description |
| --- | --- | --- |
| [Delete Product Quantity](actions/delete-product-quantity.md) | DELETE | Remove all Quantity for a Product at a specified Distribution Center. |
| [List Product Quantities](actions/list-product-quantities.md) | GET | Retrieve Quantities for a specified Product at all Distribution Centers. |
| [Update Product Quantity](actions/update-product-quantity.md) | PUT | Update Product Quantity at one or more Distribution Centers. |

### Products

| Action | Method | Description |
| --- | --- | --- |
| [Check Product Export Status](actions/check-product-export-status.md) | GET |  |
| [Check Product Upload Status](actions/check-product-upload-status.md) | GET |  |
| [Create a Product](actions/create-a-product.md) | POST |  |
| [Get Product](actions/get-product.md) | GET |  |
| [List Order Items](actions/list-order-items.md) | GET |  |
| [List Products](actions/list-products.md) | GET |  |
| [Start Product Export](actions/start-product-export.md) | POST |  |
| [Upload Product File](actions/upload-product-file.md) | POST | Should send a XML template to bulk update items |

### Profile

| Action | Method | Description |
| --- | --- | --- |
| [List Profiles](actions/list-profiles.md) | GET |  |

### Sales Orders

| Action | Method | Description |
| --- | --- | --- |
| [Create Item Fulfilment](actions/create-item-fulfilment.md) | POST | Create Item fullfilment |
| [Create Order](actions/create-order.md) | POST |  |
| [Get Order](actions/get-order.md) | GET |  |
| [List Orders](actions/list-orders.md) | GET |  |
| [Mark Order Exported](actions/post-order-exported.md) | GET | Mark an Order as Exported. |
| [Mark Order Not Exported](actions/post-order-not-exported.md) | GET | Mark an order as not exported. |
| [Ship Order](actions/ship-order.md) | PUT | Mark an entire order as shipped or partially shipped. |
| [Update Item Fullfilment](actions/update-item-fullfilment.md) | PUT | Update Item fullfilment |
| [Update Order](actions/update-order.md) | PUT | Update an Order |

### Selling Site

| Action | Method | Description |
| --- | --- | --- |
| [List Sites](actions/list-sites.md) | GET |  |


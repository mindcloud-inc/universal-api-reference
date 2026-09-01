# <img src="https://images.mindcloud.co/apps/icons/favicon-150x150_1788214513694.png" alt="Amark logo" width="28" height="28"> Amark: Universal API

Manage logistics orders, products, receipts, and suppliers

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/amarkAWL/latest
- **Actions:** 14
- **OpenAPI specification:** [openapi.json](openapi.json)

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Order Info](actions/get-order-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/amarkAWL/latest/actions/get-order-info?connectionId=$CONNECTION_ID&orderNumber=string&orderId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (14)

### Order

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Order](actions/cancel-order.md) | DELETE |  |
| [Create Order](actions/create-order.md) | POST |  |
| [Get Order Info](actions/get-order-info.md) | GET |  |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Create Products](actions/bulk-create-products.md) | POST |  |
| [Bulk Update Products](actions/bulk-update-products.md) | PUT |  |
| [Create Product](actions/create-product.md) | POST |  |
| [Get Product Info](actions/get-product-info.md) | GET |  |
| [Update Product](actions/update-product.md) | PUT |  |

### Receipt

| Action | Method | Description |
| --- | --- | --- |
| [Create Receipt](actions/create-receipt.md) | POST |  |
| [Get Receipt Info](actions/get-receipt-info.md) | GET |  |
| [Update Receipt](actions/update-receipt.md) | PUT |  |

### Supplier

| Action | Method | Description |
| --- | --- | --- |
| [Create Supplier](actions/create-supplier.md) | POST |  |
| [Get Supplier Info](actions/get-supplier-info.md) | GET |  |
| [Update Supplier](actions/update-supplier.md) | PUT |  |


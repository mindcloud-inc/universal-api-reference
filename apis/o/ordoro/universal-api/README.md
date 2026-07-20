# <img src="https://images.mindcloud.co/apps/icons/ordoro-icon-square_1775851610736.png" alt="Ordoro logo" width="28" height="28"> Ordoro: Universal API

Ordoro is an inventory, order, shipping, purchasing, and manufacturing operations platform for ecommerce teams. This app wraps the official Ordoro API for products, orders, manufacturing orders, purchase orders, suppliers, warehouses, labels, returns, and company operations.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/ordoro/latest
- **Category:** Commerce
- **Actions:** 54
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.ordoro.com
- **Vendor API docs:** https://docs.ordoro.com

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Check Authentication Status](actions/check-authentication-status.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ordoro/latest/actions/check-authentication-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (54)

### Address

| Action | Method | Description |
| --- | --- | --- |
| [Get Address by ID](actions/get-address-by-id.md) | GET | Retrieves an address from Ordoro by ID. |
| [List Addresses](actions/list-addresses.md) | GET | Retrieves addresses from Ordoro. |

### Api Key

| Action | Method | Description |
| --- | --- | --- |
| [Get API Key by ID](actions/get-api-key-by-id.md) | GET | Retrieves an API key from Ordoro by ID. |
| [List API Keys](actions/list-api-keys.md) | GET | Retrieves API keys from Ordoro. |

### Cart

| Action | Method | Description |
| --- | --- | --- |
| [Get Cart](actions/get-cart.md) | GET | Retrieves a cart from Ordoro. |
| [List Carts](actions/list-carts.md) | GET | Retrieves carts from Ordoro. |

### Comment

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Goods Receipt Comments](actions/retrieve-goods-receipt-comments.md) | GET | Retrieves comments for an Ordoro goods receipt. |
| [Retrieve Manufacturing Order Comments](actions/retrieve-manufacturing-order-comments.md) | GET | Retrieves comments for an Ordoro manufacturing order. |
| [Retrieve Order Comments](actions/retrieve-order-comments.md) | GET | Retrieves comments for an Ordoro order. |
| [Retrieve Purchase Order Comments](actions/retrieve-purchase-order-comments.md) | GET | Retrieves comments for an Ordoro purchase order. |

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Get Company Info](actions/get-company-info.md) | GET | Retrieves company information from Ordoro. |

### Connection

| Action | Method | Description |
| --- | --- | --- |
| [Check Authentication Status](actions/check-authentication-status.md) | GET | Retrieves the authentication status from Ordoro. |

### Dropship Request

| Action | Method | Description |
| --- | --- | --- |
| [Get Dropship Request for an Order](actions/get-dropship-request-for-an-order.md) | GET | Retrieves a dropship request for an Ordoro order. |

### Extra Info

| Action | Method | Description |
| --- | --- | --- |
| [Get Product Extra Info](actions/get-product-extra-info.md) | GET | Retrieves product extra information from Ordoro. |

### Goods Receipt

| Action | Method | Description |
| --- | --- | --- |
| [Get Goods Receipt by ID](actions/get-goods-receipt-by-id.md) | GET | Retrieves a goods receipt from Ordoro by ID. |
| [List Goods Receipts](actions/list-goods-receipts.md) | GET | Retrieves goods receipts from Ordoro. |

### Integration

| Action | Method | Description |
| --- | --- | --- |
| [Get Integration by ID](actions/get-integration-by-id.md) | GET | Retrieves an integration from Ordoro by ID. |
| [List Integrations](actions/list-integrations.md) | GET | Retrieves integrations from Ordoro. |

### Label

| Action | Method | Description |
| --- | --- | --- |
| [List Labels](actions/list-labels.md) | GET | Retrieves labels from Ordoro. |

### Manufacturing Order

| Action | Method | Description |
| --- | --- | --- |
| [Get Manufacturing Order by ID](actions/get-manufacturing-order-by-id.md) | GET | Retrieves a manufacturing order from Ordoro by ID. |
| [List Manufacturing Orders](actions/list-manufacturing-orders.md) | GET | Retrieves manufacturing orders from Ordoro. |

### Manufacturing Order Count

| Action | Method | Description |
| --- | --- | --- |
| [Get Manufacturing Order Counts](actions/get-manufacturing-order-counts.md) | GET | Retrieves manufacturing order counts from Ordoro. |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [Get Order](actions/get-order.md) | GET | Retrieves an order from Ordoro. |
| [List Orders](actions/list-orders.md) | GET | Retrieves orders from Ordoro. |

### Order Count

| Action | Method | Description |
| --- | --- | --- |
| [Get Order Counts](actions/get-order-counts.md) | GET | Retrieves order counts from Ordoro. |

### Packing List

| Action | Method | Description |
| --- | --- | --- |
| [Get Packing List by ID](actions/get-packing-list-by-id.md) | GET | Retrieves a packing list from Ordoro by ID. |
| [List Packing Lists](actions/list-packing-lists.md) | GET | Retrieves packing lists from Ordoro. |

### Parent Order

| Action | Method | Description |
| --- | --- | --- |
| [Get Parent Order Information](actions/get-parent-order-information.md) | GET | Retrieves parent order information from Ordoro. |

### Postage Account Balance

| Action | Method | Description |
| --- | --- | --- |
| [Get Postage Account Balance](actions/get-postage-account-balance.md) | GET | Retrieves the postage account balance from Ordoro. |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [Get Product by SKU](actions/get-product-by-sku.md) | GET | Retrieves a product from Ordoro by SKU. |
| [List Products](actions/list-products.md) | GET | Retrieves products from Ordoro. |

### Product Cart Bridge

| Action | Method | Description |
| --- | --- | --- |
| [Get Product Cart Bridge](actions/get-product-cart-bridge.md) | GET | Retrieves product cart bridge data from Ordoro. |

### Product Image

| Action | Method | Description |
| --- | --- | --- |
| [Get Product Images](actions/get-product-images.md) | GET | Retrieves product images from Ordoro. |

### Product Kit Graph

| Action | Method | Description |
| --- | --- | --- |
| [Get Product Kit Graph](actions/get-product-kit-graph.md) | GET | Retrieves a product kit graph from Ordoro. |

### Product Tag

| Action | Method | Description |
| --- | --- | --- |
| [Get Product Tag by Name](actions/get-product-tag-by-name.md) | GET | Retrieves a product tag from Ordoro by name. |
| [List Product Tags](actions/list-product-tags.md) | GET | Retrieves product tags from Ordoro. |

### Purchase Order

| Action | Method | Description |
| --- | --- | --- |
| [Get Purchase Order by ID](actions/get-purchase-order-by-id.md) | GET | Retrieves a purchase order from Ordoro by ID. |
| [List Purchase Orders](actions/list-purchase-orders.md) | GET | Retrieves purchase orders from Ordoro. |

### Purchase Order Count

| Action | Method | Description |
| --- | --- | --- |
| [Get Purchase Order Counts](actions/get-purchase-order-counts.md) | GET | Retrieves purchase order counts from Ordoro. |

### Purchase Order Preview

| Action | Method | Description |
| --- | --- | --- |
| [Preview Purchase Order](actions/preview-purchase-order.md) | GET | Retrieves a purchase order preview from Ordoro. |

### Return Tracking

| Action | Method | Description |
| --- | --- | --- |
| [Get Return Tracking by ID](actions/get-return-tracking-by-id.md) | GET | Retrieves a return tracking from Ordoro by ID. |
| [List Return Trackings](actions/list-return-trackings.md) | GET | Retrieves return trackings from Ordoro. |

### Rule

| Action | Method | Description |
| --- | --- | --- |
| [Get Rule by ID](actions/get-rule-by-id.md) | GET | Retrieves a rule from Ordoro by ID. |
| [List Rules](actions/list-rules.md) | GET | Retrieves rules from Ordoro. |

### Shipper

| Action | Method | Description |
| --- | --- | --- |
| [Get Shipper by ID](actions/get-shipper-by-id.md) | GET | Retrieves a shipper from Ordoro by ID. |
| [List Shippers](actions/list-shippers.md) | GET | Retrieves shippers from Ordoro. |

### Supplier

| Action | Method | Description |
| --- | --- | --- |
| [Get Supplier by ID](actions/get-supplier-by-id.md) | GET | Retrieves a supplier from Ordoro by ID. |
| [List Suppliers](actions/list-suppliers.md) | GET | Retrieves suppliers from Ordoro. |

### Supplier Shipping Method

| Action | Method | Description |
| --- | --- | --- |
| [Get Supplier Shipping Methods](actions/get-supplier-shipping-methods.md) | GET | Retrieves supplier shipping methods from Ordoro. |

### Sync State

| Action | Method | Description |
| --- | --- | --- |
| [Get Cart Sync Setting](actions/get-cart-sync-setting.md) | GET | Retrieves cart sync settings from Ordoro. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from Ordoro. |
| [Get User by ID](actions/get-user-by-id.md) | GET | Retrieves a user from Ordoro by ID. |
| [List Users](actions/list-users.md) | GET | Retrieves users from Ordoro. |

### Warehouse

| Action | Method | Description |
| --- | --- | --- |
| [Get Cart Warehouses](actions/get-cart-warehouses.md) | GET | Retrieves warehouses for an Ordoro cart. |


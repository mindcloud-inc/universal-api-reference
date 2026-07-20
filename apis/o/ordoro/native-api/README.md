# Ordoro: Native API Reference

A consolidated summary of Ordoro's API configuration and 54 documented operations, with links to official documentation.

- **Official docs:** https://docs.ordoro.com
- **API base URL:** `https://api.ordoro.com`

## Authentication

### Ordoro Basic Auth

Use the Client ID as the basic-auth username and the Client Secret as the basic-auth password for Ordoro API requests.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://docs.ordoro.com)

## Pagination

Use `limit` in the query string to set the page size (default 10; accepted range 1–100). Use `offset` in the query string as the record offset; numbering starts at 0.

## Sorting

Set the sort field with `sort` in the query string. Only one sort field is accepted.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (54 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check Authentication Status](actions/check-authentication-status.md) | `GET /authenticated/` | [docs](https://docs.ordoro.com) |
| [Get Address by ID](actions/get-address-by-id.md) | `GET /address/{address_id}/` | [docs](https://docs.ordoro.com) |
| [Get API Key by ID](actions/get-api-key-by-id.md) | `GET /api_key/{api_key_id}/` | [docs](https://docs.ordoro.com) |
| [Get Cart](actions/get-cart.md) | `GET /cart/{cart_id}/` | [docs](https://docs.ordoro.com) |
| [Get Cart Sync Setting](actions/get-cart-sync-setting.md) | `GET /cart/{cart_id}/autosync/` | [docs](https://docs.ordoro.com) |
| [Get Cart Warehouses](actions/get-cart-warehouses.md) | `GET /cart/{cart_id}/warehouse/` | [docs](https://docs.ordoro.com) |
| [Get Company Info](actions/get-company-info.md) | `GET /company/` | [docs](https://docs.ordoro.com) |
| [Get Current User](actions/get-current-user.md) | `GET /user/me/` | [docs](https://docs.ordoro.com) |
| [Get Dropship Request for an Order](actions/get-dropship-request-for-an-order.md) | `GET /v3/order/{order_number}/dropship` | [docs](https://docs.ordoro.com) |
| [Get Goods Receipt by ID](actions/get-goods-receipt-by-id.md) | `GET /goods_receipt/{goods_receipt_id}/` | [docs](https://docs.ordoro.com) |
| [Get Integration by ID](actions/get-integration-by-id.md) | `GET /integration/{integration_id}/` | [docs](https://docs.ordoro.com) |
| [Get Manufacturing Order by ID](actions/get-manufacturing-order-by-id.md) | `GET /v3/manufacturing_order/{reference_id}` | [docs](https://docs.ordoro.com) |
| [Get Manufacturing Order Counts](actions/get-manufacturing-order-counts.md) | `GET /v3/manufacturing_order/counts` | [docs](https://docs.ordoro.com) |
| [Get Order](actions/get-order.md) | `GET /v3/order/{order_number}` | [docs](https://docs.ordoro.com) |
| [Get Order Counts](actions/get-order-counts.md) | `GET /v3/order/counts` | [docs](https://docs.ordoro.com) |
| [Get Packing List by ID](actions/get-packing-list-by-id.md) | `GET /packing_list/{packing_list_id}/` | [docs](https://docs.ordoro.com) |
| [Get Parent Order Information](actions/get-parent-order-information.md) | `GET /v3/order/parent/{parent_order_number}` | [docs](https://docs.ordoro.com) |
| [Get Postage Account Balance](actions/get-postage-account-balance.md) | `GET /v3/account/balance` | [docs](https://docs.ordoro.com) |
| [Get Product by SKU](actions/get-product-by-sku.md) | `GET /product/{sku}/` | [docs](https://docs.ordoro.com) |
| [Get Product Cart Bridge](actions/get-product-cart-bridge.md) | `GET /product/{sku}/cart/{cart_id}/` | [docs](https://docs.ordoro.com) |
| [Get Product Extra Info](actions/get-product-extra-info.md) | `GET /product/{sku}/cart/{cart_id}/extra_info/` | [docs](https://docs.ordoro.com) |
| [Get Product Images](actions/get-product-images.md) | `GET /product/{sku}/image/` | [docs](https://docs.ordoro.com) |
| [Get Product Kit Graph](actions/get-product-kit-graph.md) | `GET /product/{sku}/kit_graph/` | [docs](https://docs.ordoro.com) |
| [Get Product Tag by Name](actions/get-product-tag-by-name.md) | `GET /product/tag/{tagNamePath}/` | [docs](https://docs.ordoro.com) |
| [Get Purchase Order by ID](actions/get-purchase-order-by-id.md) | `GET /purchase_order/{po_id}/` | [docs](https://docs.ordoro.com) |
| [Get Purchase Order Counts](actions/get-purchase-order-counts.md) | `GET /purchase_order/counts/` | [docs](https://docs.ordoro.com) |
| [Get Return Tracking by ID](actions/get-return-tracking-by-id.md) | `GET /return_tracking/{return_tracking_id}/` | [docs](https://docs.ordoro.com) |
| [Get Rule by ID](actions/get-rule-by-id.md) | `GET /rule/{rule_id}/` | [docs](https://docs.ordoro.com) |
| [Get Shipper by ID](actions/get-shipper-by-id.md) | `GET /shipper/{shipper_id}/` | [docs](https://docs.ordoro.com) |
| [Get Supplier by ID](actions/get-supplier-by-id.md) | `GET /supplier/{supplier_id}/` | [docs](https://docs.ordoro.com) |
| [Get Supplier Shipping Methods](actions/get-supplier-shipping-methods.md) | `GET /supplier/{supplier_id}/shipping_methods/` | [docs](https://docs.ordoro.com) |
| [Get User by ID](actions/get-user-by-id.md) | `GET /user/{user_id}/` | [docs](https://docs.ordoro.com) |
| [List Addresses](actions/list-addresses.md) | `GET /address/` | [docs](https://docs.ordoro.com) |
| [List API Keys](actions/list-api-keys.md) | `GET /api_key/` | [docs](https://docs.ordoro.com) |
| [List Carts](actions/list-carts.md) | `GET /cart/` | [docs](https://docs.ordoro.com) |
| [List Goods Receipts](actions/list-goods-receipts.md) | `GET /goods_receipt/` | [docs](https://docs.ordoro.com) |
| [List Integrations](actions/list-integrations.md) | `GET /integration/` | [docs](https://docs.ordoro.com) |
| [List Labels](actions/list-labels.md) | `GET /v3/label` | [docs](https://docs.ordoro.com) |
| [List Manufacturing Orders](actions/list-manufacturing-orders.md) | `GET /v3/manufacturing_order` | [docs](https://docs.ordoro.com) |
| [List Orders](actions/list-orders.md) | `GET /v3/order` | [docs](https://docs.ordoro.com) |
| [List Packing Lists](actions/list-packing-lists.md) | `GET /packing_list/` | [docs](https://docs.ordoro.com) |
| [List Product Tags](actions/list-product-tags.md) | `GET /product/tag/` | [docs](https://docs.ordoro.com) |
| [List Products](actions/list-products.md) | `GET /product/` | [docs](https://docs.ordoro.com) |
| [List Purchase Orders](actions/list-purchase-orders.md) | `GET /purchase_order/` | [docs](https://docs.ordoro.com) |
| [List Return Trackings](actions/list-return-trackings.md) | `GET /return_tracking/` | [docs](https://docs.ordoro.com) |
| [List Rules](actions/list-rules.md) | `GET /rule/` | [docs](https://docs.ordoro.com) |
| [List Shippers](actions/list-shippers.md) | `GET /shipper/` | [docs](https://docs.ordoro.com) |
| [List Suppliers](actions/list-suppliers.md) | `GET /supplier/` | [docs](https://docs.ordoro.com) |
| [List Users](actions/list-users.md) | `GET /user/` | [docs](https://docs.ordoro.com) |
| [Preview Purchase Order](actions/preview-purchase-order.md) | `GET /purchase_order/{po_id}/send/` | [docs](https://docs.ordoro.com) |
| [Retrieve Goods Receipt Comments](actions/retrieve-goods-receipt-comments.md) | `GET /goods_receipt/{goods_receipt_id}/comment/` | [docs](https://docs.ordoro.com) |
| [Retrieve Manufacturing Order Comments](actions/retrieve-manufacturing-order-comments.md) | `GET /v3/manufacturing_order/{reference_id}/comment` | [docs](https://docs.ordoro.com) |
| [Retrieve Order Comments](actions/retrieve-order-comments.md) | `GET /v3/order/{order_number}/comment` | [docs](https://docs.ordoro.com) |
| [Retrieve Purchase Order Comments](actions/retrieve-purchase-order-comments.md) | `GET /purchase_order/{po_id}/comment/` | [docs](https://docs.ordoro.com) |

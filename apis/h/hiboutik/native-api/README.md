# Hiboutik: Native API Reference

A consolidated summary of Hiboutik's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://mindcloudhiboutik20260402.hiboutik.com/docapi/
- **OpenAPI specification:** https://mindcloudhiboutik20260402.hiboutik.com/docapi/json/
- **API base URL:** `https://mindcloudhiboutik20260402.hiboutik.com/api`

## Authentication

### Basic Auth

Use your Hiboutik API login email as the username and your tenant API key as the password.

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

[Official authentication documentation](https://faq.hiboutik.com/fr/api-developpement/api-getting-started-authorization-api-credentials)

## Pagination

Use `p` in the query string to choose the page; numbering starts at 1.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Calendar Event](actions/get-calendar-event.md) | `GET /calendar/event/:event_id` | [docs](https://mindcloudhiboutik20260402.hiboutik.com/docapi/) |
| [Get Customer](actions/get-customer.md) | `GET /customer/:customers_id` | [docs](https://mindcloudhiboutik20260402.hiboutik.com/docapi/) |
| [Get Customer Address](actions/get-customer-address.md) | `GET /customers_addresses/:address_id` | [docs](https://mindcloudhiboutik20260402.hiboutik.com/docapi/) |
| [Get First Closed Sale](actions/get-first-closed-sale.md) | `GET /first_closed_sale/:store_id` | [docs](https://mindcloudhiboutik20260402.hiboutik.com/docapi/) |
| [Get Product](actions/get-product.md) | `GET /products/:product_id` | [docs](https://mindcloudhiboutik20260402.hiboutik.com/docapi/) |
| [Get Product Barcode](actions/get-product-barcode.md) | `GET /products_barcode/:store_id/:product_id/:size_id/` | [docs](https://mindcloudhiboutik20260402.hiboutik.com/docapi/) |
| [Get Sale](actions/get-sale.md) | `GET /sales/:sale_id` | [docs](https://mindcloudhiboutik20260402.hiboutik.com/docapi/) |
| [Get Stock Order](actions/get-stock-order.md) | `GET /inventory_inputs/:inventory_input_id` | [docs](https://mindcloudhiboutik20260402.hiboutik.com/docapi/) |
| [Get Stock Transfer](actions/get-stock-transfer.md) | `GET /stock_transfer/:transfer_id` | [docs](https://mindcloudhiboutik20260402.hiboutik.com/docapi/) |
| [List Brands](actions/list-brands.md) | `GET /brands` | [docs](https://mindcloudhiboutik20260402.hiboutik.com/docapi/) |
| [List Calendar Events](actions/list-calendar-events.md) | `GET /calendar/events/:store_id/:year/:month/:day` | [docs](https://mindcloudhiboutik20260402.hiboutik.com/docapi/) |
| [List Cash Movements](actions/list-cash-movements.md) | `GET /till/:store_id/:year/:month` | [docs](https://mindcloudhiboutik20260402.hiboutik.com/docapi/) |
| [List Categories](actions/list-categories.md) | `GET /categories` | [docs](https://mindcloudhiboutik20260402.hiboutik.com/docapi/) |
| [List Closed Sales](actions/list-closed-sales.md) | `GET /closed_sales/:store_id/:year/:month/:day` | [docs](https://mindcloudhiboutik20260402.hiboutik.com/docapi/) |
| [List Customer Prepaid Purchase Lines](actions/list-customer-prepaid-purchase-lines.md) | `GET /prepaid_purchases/:customers_id` | [docs](https://mindcloudhiboutik20260402.hiboutik.com/docapi/) |
| [List Customers](actions/list-customers.md) | `GET /customers/` | [docs](https://mindcloudhiboutik20260402.hiboutik.com/docapi/) |
| [List Kitchen Cooking Stations](actions/list-kitchen-cooking-stations.md) | `GET /kitchen/cooking_stations` | [docs](https://mindcloudhiboutik20260402.hiboutik.com/docapi/) |
| [List Kitchen Open Tables](actions/list-kitchen-open-tables.md) | `GET /kitchen/open_tables` | [docs](https://mindcloudhiboutik20260402.hiboutik.com/docapi/) |
| [List Modifiers](actions/list-modifiers.md) | `GET /modifiers/` | [docs](https://mindcloudhiboutik20260402.hiboutik.com/docapi/) |
| [List Open Sales](actions/list-open-sales.md) | `GET /open_sales/:store_id` | [docs](https://mindcloudhiboutik20260402.hiboutik.com/docapi/) |
| [List Payment Types](actions/list-payment-types.md) | `GET /payment_types/:store_id/` | [docs](https://mindcloudhiboutik20260402.hiboutik.com/docapi/) |
| [List Pending Credit Notes](actions/list-pending-credit-notes.md) | `GET /credit_notes/:store_id` | [docs](https://mindcloudhiboutik20260402.hiboutik.com/docapi/) |
| [List Prepaid Purchase Lines](actions/list-prepaid-purchase-lines.md) | `GET /prepaid_purchases/` | [docs](https://mindcloudhiboutik20260402.hiboutik.com/docapi/) |
| [List Product Purchased History](actions/list-product-purchased-history.md) | `GET /product_purchased_history/:product_id/` | [docs](https://mindcloudhiboutik20260402.hiboutik.com/docapi/) |
| [List Products](actions/list-products.md) | `GET /products/` | [docs](https://mindcloudhiboutik20260402.hiboutik.com/docapi/) |
| [List Products Purchased](actions/list-products-purchased.md) | `GET /products_purchased/:warehouse_id/:year/:month/:day/` | [docs](https://mindcloudhiboutik20260402.hiboutik.com/docapi/) |
| [List Products Returned](actions/list-products-returned.md) | `GET /products_returned/:store_id/:year/:month/:day` | [docs](https://mindcloudhiboutik20260402.hiboutik.com/docapi/) |
| [List Products Sold](actions/list-products-sold.md) | `GET /products_sold/:store_id/:year/:month/:day/` | [docs](https://mindcloudhiboutik20260402.hiboutik.com/docapi/) |
| [List Stock Order Details](actions/list-stock-order-details.md) | `GET /inventory_input_details/:inventory_input_id` | [docs](https://mindcloudhiboutik20260402.hiboutik.com/docapi/) |
| [List Stock Order Details on Hold](actions/list-stock-order-details-on-hold.md) | `GET /inventory_inputs_on_hold/` | [docs](https://mindcloudhiboutik20260402.hiboutik.com/docapi/) |
| [List Stock Orders](actions/list-stock-orders.md) | `GET /inventory_inputs/` | [docs](https://mindcloudhiboutik20260402.hiboutik.com/docapi/) |
| [List Stock Transfer Details](actions/list-stock-transfer-details.md) | `GET /stock_transfer_details/:transfer_id` | [docs](https://mindcloudhiboutik20260402.hiboutik.com/docapi/) |
| [List Stock Transfers](actions/list-stock-transfers.md) | `GET /stock_transfer/` | [docs](https://mindcloudhiboutik20260402.hiboutik.com/docapi/) |
| [List Stores](actions/list-stores.md) | `GET /stores` | [docs](https://mindcloudhiboutik20260402.hiboutik.com/docapi/) |
| [List Subscriptions](actions/list-subscriptions.md) | `GET /subscriptions` | [docs](https://mindcloudhiboutik20260402.hiboutik.com/docapi/) |
| [List Suppliers](actions/list-suppliers.md) | `GET /suppliers/` | [docs](https://mindcloudhiboutik20260402.hiboutik.com/docapi/) |
| [List Taxes](actions/list-taxes.md) | `GET /taxes` | [docs](https://mindcloudhiboutik20260402.hiboutik.com/docapi/) |
| [List Warehouses](actions/list-warehouses.md) | `GET /warehouses` | [docs](https://mindcloudhiboutik20260402.hiboutik.com/docapi/) |
| [Search Products By Barcode](actions/search-products-by-barcode.md) | `GET /products/search/barcode/:q/` | [docs](https://mindcloudhiboutik20260402.hiboutik.com/docapi/) |
| [Search Products By Name](actions/search-products-by-name.md) | `GET /products/search/name/:q` | [docs](https://mindcloudhiboutik20260402.hiboutik.com/docapi/) |

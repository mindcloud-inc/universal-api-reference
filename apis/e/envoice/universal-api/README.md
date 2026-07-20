# <img src="https://images.mindcloud.co/apps/icons/envoice-icon_1776695816086.png" alt="Envoice logo" width="28" height="28"> Envoice: Universal API

Envoice helps businesses manage clients, invoices, work types, taxes, payment providers, and supporting reference data through its REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/envoice/latest
- **Category:** Commerce / Payments & Billing
- **Actions:** 61
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.envoice.in
- **Vendor API docs:** https://www.envoice.in/reference/api/docs/v1

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Countries](actions/list-countries.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/envoice/latest/actions/list-countries?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (61)

### Categories

| Action | Method | Description |
| --- | --- | --- |
| [Create Invoice Category](actions/create-invoice-category.md) | POST | Creates a new invoice category in Envoice. |
| [Delete Invoice Category](actions/delete-invoice-category.md) | DELETE | Deletes an existing invoice category from Envoice. |
| [List Invoice Categories](actions/list-invoice-categories.md) | GET | Retrieves invoice categories from Envoice. |
| [Update Invoice Category](actions/update-invoice-category.md) | PUT | Updates an existing invoice category in Envoice. |

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [Can Delete Client](actions/can-delete-client.md) | GET | Checks whether a client can be deleted in Envoice. |
| [Create Client](actions/create-client.md) | POST | Creates a new client in Envoice. |
| [Delete Client](actions/delete-client.md) | DELETE | Deletes an existing client from Envoice. |
| [Get Client Details](actions/get-client-details.md) | GET | Retrieves client details from Envoice. |
| [List Clients](actions/list-clients.md) | GET | Retrieves clients from Envoice. |
| [Update Client](actions/update-client.md) | PUT | Updates an existing client in Envoice. |

### Estimates

| Action | Method | Description |
| --- | --- | --- |
| [Change Estimation Status](actions/change-estimation-status.md) | PUT | Updates an estimation status in Envoice. |
| [Create Estimation](actions/create-estimation.md) | POST | Creates a new estimation in Envoice. |
| [Delete Estimation](actions/delete-estimation.md) | DELETE | Deletes an existing estimation from Envoice. |
| [Get Estimation Details](actions/get-estimation-details.md) | GET | Retrieves estimation details from Envoice. |
| [Get Estimation Share URI](actions/get-estimation-share-uri.md) | GET | Retrieves a shared estimation URL from Envoice. |
| [Get Estimation Status](actions/get-estimation-status.md) | GET | Retrieves an estimation status from Envoice. |
| [List Estimations](actions/list-estimations.md) | GET | Retrieves estimations from Envoice. |
| [Send Estimation to Client](actions/send-estimation-to-client.md) | PUT | Sends an estimation to a client in Envoice. |
| [Update Estimation](actions/update-estimation.md) | PUT | Updates an existing estimation in Envoice. |

### Invoices

| Action | Method | Description |
| --- | --- | --- |
| [Change Invoice Status](actions/change-invoice-status.md) | PUT | Updates an invoice status in Envoice. |
| [Convert Estimation to Invoice](actions/convert-estimation-to-invoice.md) | POST | Converts an estimation to an invoice in Envoice. |
| [Create Invoice](actions/create-invoice.md) | POST | Creates a new invoice in Envoice. |
| [Delete Invoice](actions/delete-invoice.md) | DELETE | Deletes an existing invoice from Envoice. |
| [Get Invoice Details](actions/get-invoice-details.md) | GET | Retrieves invoice details from Envoice. |
| [Get Invoice PDF Link](actions/get-invoice-pdf-link.md) | GET | Retrieves an invoice PDF URL from Envoice. |
| [Get Invoice Share URI](actions/get-invoice-share-uri.md) | GET | Retrieves a shared invoice URL from Envoice. |
| [Get Invoice Status](actions/get-invoice-status.md) | GET | Retrieves an invoice status from Envoice. |
| [List Invoices](actions/list-invoices.md) | GET | Retrieves invoices from Envoice. |
| [Send Invoice to Accountant](actions/send-invoice-to-accountant.md) | PUT | Sends an invoice to an accountant in Envoice. |
| [Send Invoice to Client](actions/send-invoice-to-client.md) | PUT | Sends an invoice to a client in Envoice. |
| [Update Invoice](actions/update-invoice.md) | PUT | Updates an existing invoice in Envoice. |

### Orders

| Action | Method | Description |
| --- | --- | --- |
| [Change Order Shipping Details](actions/change-order-shipping-details.md) | PUT | Updates order shipping details in Envoice. |
| [Change Order Status](actions/change-order-status.md) | PUT | Updates an order status in Envoice. |
| [Create Order](actions/create-order.md) | POST | Creates a new order in Envoice. |
| [Delete Order](actions/delete-order.md) | DELETE | Deletes an existing order from Envoice. |
| [Get Order Details](actions/get-order-details.md) | GET | Retrieves order details from Envoice. |
| [List Orders](actions/list-orders.md) | GET | Retrieves orders from Envoice. |

### Payment Intents

| Action | Method | Description |
| --- | --- | --- |
| [Create Payment Link](actions/create-payment-link.md) | POST | Creates a new payment link in Envoice. |
| [Delete Payment Link](actions/delete-payment-link.md) | DELETE | Deletes an existing payment link from Envoice. |
| [Get Payment Link URI](actions/get-payment-link-uri.md) | GET | Retrieves a payment link URL from Envoice. |
| [List Payment Links](actions/list-payment-links.md) | GET | Retrieves payment links from Envoice. |

### Payment Methods

| Action | Method | Description |
| --- | --- | --- |
| [List Supported Payment Providers](actions/list-supported-payment-providers.md) | GET | Retrieves supported payment providers from Envoice. |

### Products

| Action | Method | Description |
| --- | --- | --- |
| [Create Product](actions/create-product.md) | POST | Creates a new product in Envoice. |
| [Delete Product](actions/delete-product.md) | DELETE | Deletes an existing product from Envoice. |
| [Get Product Details](actions/get-product-details.md) | GET | Retrieves product details from Envoice. |
| [List Products](actions/list-products.md) | GET | Retrieves products from Envoice. |
| [Update Product](actions/update-product.md) | PUT | Updates an existing product in Envoice. |

### Services

| Action | Method | Description |
| --- | --- | --- |
| [Create Work Type](actions/create-work-type.md) | POST | Creates a new work type in Envoice. |
| [Delete Work Type](actions/delete-work-type.md) | DELETE | Deletes an existing work type from Envoice. |
| [Get Work Type Details](actions/get-work-type-details.md) | GET | Retrieves work type details from Envoice. |
| [List Work Types](actions/list-work-types.md) | GET | Retrieves work types from Envoice. |
| [Search Work Types](actions/search-work-types.md) | GET | Finds work types in Envoice by query. |
| [Update Work Type](actions/update-work-type.md) | PUT | Updates an existing work type in Envoice. |

### Tax Rates

| Action | Method | Description |
| --- | --- | --- |
| [Create Tax Rate](actions/create-tax-rate.md) | POST | Creates a new tax rate in Envoice. |
| [Delete Tax Rate](actions/delete-tax-rate.md) | DELETE | Deletes an existing tax rate from Envoice. |
| [List Tax Rates](actions/list-tax-rates.md) | GET | Retrieves tax rates from Envoice. |
| [Update Tax Rate](actions/update-tax-rate.md) | PUT | Updates an existing tax rate in Envoice. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [List Countries](actions/list-countries.md) | GET | Retrieves supported countries from Envoice. |
| [List Currencies](actions/list-currencies.md) | GET | Retrieves supported currencies from Envoice. |
| [List Date Formats](actions/list-date-formats.md) | GET | Retrieves supported date formats from Envoice. |
| [List UI Languages](actions/list-ui-languages.md) | GET | Retrieves supported UI languages from Envoice. |


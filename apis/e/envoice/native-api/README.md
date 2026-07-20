# Envoice: Native API Reference

A consolidated summary of Envoice's API configuration and 61 documented operations, with links to official documentation.

- **Official docs:** https://www.envoice.in/reference/api/docs/v1
- **API base URL:** `https://www.envoice.in/api`

## Authentication

### API Credentials

Use the API Key and Secret Key from Envoice account settings. Requests send them as x-auth-key and x-auth-secret headers.

### Credentials

- **Auth Key:** `authKey` · required · Your Envoice API Key from account settings.
- **Auth Secret:** `authSecret` · required · Your Envoice Secret Key from account settings.

Send these headers with each API request:

```http
x-auth-key: <authKey>
x-auth-secret: <authSecret>
```

[Official authentication documentation](https://www.envoice.in/account/settings#api-tab)

## Endpoints (61 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Can Delete Client](actions/can-delete-client.md) | `GET client/candelete` | [docs](https://www.envoice.in/reference/api/docs/v1) |
| [Change Estimation Status](actions/change-estimation-status.md) | `POST estimation/changestatus` | [docs](https://www.envoice.in/reference/api/docs/v1) |
| [Change Invoice Status](actions/change-invoice-status.md) | `POST invoice/changestatus` | [docs](https://github.com/EmitKnowledge/Envoice/blob/master/invoice.md) |
| [Change Order Shipping Details](actions/change-order-shipping-details.md) | `POST order/changeshippingdetails` | [docs](https://www.envoice.in/reference/api/docs/v1) |
| [Change Order Status](actions/change-order-status.md) | `POST order/changestatus` | [docs](https://www.envoice.in/reference/api/docs/v1) |
| [Convert Estimation to Invoice](actions/convert-estimation-to-invoice.md) | `POST estimation/convert` | [docs](https://www.envoice.in/reference/api/docs/v1) |
| [Create Client](actions/create-client.md) | `POST client/new` | [docs](https://github.com/EmitKnowledge/Envoice/blob/master/client.md) |
| [Create Estimation](actions/create-estimation.md) | `POST estimation/new` | [docs](https://www.envoice.in/reference/api/docs/v1) |
| [Create Invoice](actions/create-invoice.md) | `POST invoice/new` | [docs](https://github.com/EmitKnowledge/Envoice/blob/master/invoice.md) |
| [Create Invoice Category](actions/create-invoice-category.md) | `POST invoice/newcategory` | [docs](https://www.envoice.in/reference/api/docs/v1) |
| [Create Order](actions/create-order.md) | `POST order/new` | [docs](https://www.envoice.in/reference/api/docs/v1) |
| [Create Payment Link](actions/create-payment-link.md) | `POST paymentlink/new` | [docs](https://www.envoice.in/reference/api/docs/v1) |
| [Create Product](actions/create-product.md) | `POST product/new` | [docs](https://www.envoice.in/reference/api/docs/v1) |
| [Create Tax Rate](actions/create-tax-rate.md) | `POST tax/new` | [docs](https://github.com/EmitKnowledge/Envoice/blob/master/tax.md) |
| [Create Work Type](actions/create-work-type.md) | `POST worktype/new` | [docs](https://github.com/EmitKnowledge/Envoice/blob/master/work-type.md) |
| [Delete Client](actions/delete-client.md) | `POST client/delete` | [docs](https://github.com/EmitKnowledge/Envoice/blob/master/client.md) |
| [Delete Estimation](actions/delete-estimation.md) | `POST estimation/delete` | [docs](https://www.envoice.in/reference/api/docs/v1) |
| [Delete Invoice](actions/delete-invoice.md) | `POST invoice/delete` | [docs](https://github.com/EmitKnowledge/Envoice/blob/master/invoice.md) |
| [Delete Invoice Category](actions/delete-invoice-category.md) | `POST invoice/deletecategory` | [docs](https://www.envoice.in/reference/api/docs/v1) |
| [Delete Order](actions/delete-order.md) | `POST order/delete` | [docs](https://www.envoice.in/reference/api/docs/v1) |
| [Delete Payment Link](actions/delete-payment-link.md) | `POST paymentlink/delete` | [docs](https://www.envoice.in/reference/api/docs/v1) |
| [Delete Product](actions/delete-product.md) | `POST product/delete` | [docs](https://www.envoice.in/reference/api/docs/v1) |
| [Delete Tax Rate](actions/delete-tax-rate.md) | `POST tax/delete` | [docs](https://github.com/EmitKnowledge/Envoice/blob/master/tax.md) |
| [Delete Work Type](actions/delete-work-type.md) | `POST worktype/delete` | [docs](https://github.com/EmitKnowledge/Envoice/blob/master/work-type.md) |
| [Get Client Details](actions/get-client-details.md) | `GET client/details` | [docs](https://www.envoice.in/reference/api/docs/v1) |
| [Get Estimation Details](actions/get-estimation-details.md) | `GET estimation/details` | [docs](https://www.envoice.in/reference/api/docs/v1) |
| [Get Estimation Share URI](actions/get-estimation-share-uri.md) | `GET estimation/uri` | [docs](https://www.envoice.in/reference/api/docs/v1) |
| [Get Estimation Status](actions/get-estimation-status.md) | `GET estimation/status` | [docs](https://www.envoice.in/reference/api/docs/v1) |
| [Get Invoice Details](actions/get-invoice-details.md) | `GET invoice/details` | [docs](https://github.com/EmitKnowledge/Envoice/blob/master/invoice.md) |
| [Get Invoice PDF Link](actions/get-invoice-pdf-link.md) | `GET invoice/pdf` | [docs](https://www.envoice.in/reference/api/docs/v1) |
| [Get Invoice Share URI](actions/get-invoice-share-uri.md) | `GET invoice/uri` | [docs](https://github.com/EmitKnowledge/Envoice/blob/master/invoice.md) |
| [Get Invoice Status](actions/get-invoice-status.md) | `GET invoice/status` | [docs](https://github.com/EmitKnowledge/Envoice/blob/master/invoice.md) |
| [Get Order Details](actions/get-order-details.md) | `GET order/details` | [docs](https://www.envoice.in/reference/api/docs/v1) |
| [Get Payment Link URI](actions/get-payment-link-uri.md) | `GET paymentlink/uri` | [docs](https://www.envoice.in/reference/api/docs/v1) |
| [Get Product Details](actions/get-product-details.md) | `GET product/details` | [docs](https://www.envoice.in/reference/api/docs/v1) |
| [Get Work Type Details](actions/get-work-type-details.md) | `GET worktype/details` | [docs](https://www.envoice.in/reference/api/docs/v1) |
| [List Clients](actions/list-clients.md) | `GET client/all` | [docs](https://github.com/EmitKnowledge/Envoice/blob/master/client.md) |
| [List Countries](actions/list-countries.md) | `GET general/countries` | [docs](https://github.com/EmitKnowledge/Envoice/blob/master/general.md) |
| [List Currencies](actions/list-currencies.md) | `GET general/currencies` | [docs](https://github.com/EmitKnowledge/Envoice/blob/master/general.md) |
| [List Date Formats](actions/list-date-formats.md) | `GET general/dateformats` | [docs](https://www.envoice.in/reference/api/docs/v1) |
| [List Estimations](actions/list-estimations.md) | `GET estimation/all` | [docs](https://www.envoice.in/reference/api/docs/v1) |
| [List Invoice Categories](actions/list-invoice-categories.md) | `GET invoice/allcategories` | [docs](https://www.envoice.in/reference/api/docs/v1) |
| [List Invoices](actions/list-invoices.md) | `GET invoice/all` | [docs](https://github.com/EmitKnowledge/Envoice/blob/master/invoice.md) |
| [List Orders](actions/list-orders.md) | `GET order/all` | [docs](https://www.envoice.in/reference/api/docs/v1) |
| [List Payment Links](actions/list-payment-links.md) | `GET paymentlink/all` | [docs](https://www.envoice.in/reference/api/docs/v1) |
| [List Products](actions/list-products.md) | `GET product/all` | [docs](https://www.envoice.in/reference/api/docs/v1) |
| [List Supported Payment Providers](actions/list-supported-payment-providers.md) | `GET payment/supported` | [docs](https://github.com/EmitKnowledge/Envoice/blob/master/payment.md) |
| [List Tax Rates](actions/list-tax-rates.md) | `GET tax/all` | [docs](https://github.com/EmitKnowledge/Envoice/blob/master/tax.md) |
| [List UI Languages](actions/list-ui-languages.md) | `GET general/uilanguages` | [docs](https://github.com/EmitKnowledge/Envoice/blob/master/general.md) |
| [List Work Types](actions/list-work-types.md) | `GET worktype/all` | [docs](https://github.com/EmitKnowledge/Envoice/blob/master/work-type.md) |
| [Search Work Types](actions/search-work-types.md) | `GET worktype/search` | [docs](https://www.envoice.in/reference/api/docs/v1) |
| [Send Estimation to Client](actions/send-estimation-to-client.md) | `POST estimation/sendtoclient` | [docs](https://www.envoice.in/reference/api/docs/v1) |
| [Send Invoice to Accountant](actions/send-invoice-to-accountant.md) | `POST invoice/sendtoaccountant` | [docs](https://github.com/EmitKnowledge/Envoice/blob/master/invoice.md) |
| [Send Invoice to Client](actions/send-invoice-to-client.md) | `POST invoice/sendtoclient` | [docs](https://github.com/EmitKnowledge/Envoice/blob/master/invoice.md) |
| [Update Client](actions/update-client.md) | `POST client/update` | [docs](https://github.com/EmitKnowledge/Envoice/blob/master/client.md) |
| [Update Estimation](actions/update-estimation.md) | `POST estimation/update` | [docs](https://www.envoice.in/reference/api/docs/v1) |
| [Update Invoice](actions/update-invoice.md) | `POST invoice/update` | [docs](https://github.com/EmitKnowledge/Envoice/blob/master/invoice.md) |
| [Update Invoice Category](actions/update-invoice-category.md) | `POST invoice/updatecategory` | [docs](https://www.envoice.in/reference/api/docs/v1) |
| [Update Product](actions/update-product.md) | `POST product/update` | [docs](https://www.envoice.in/reference/api/docs/v1) |
| [Update Tax Rate](actions/update-tax-rate.md) | `POST tax/update` | [docs](https://github.com/EmitKnowledge/Envoice/blob/master/tax.md) |
| [Update Work Type](actions/update-work-type.md) | `POST worktype/update` | [docs](https://github.com/EmitKnowledge/Envoice/blob/master/work-type.md) |

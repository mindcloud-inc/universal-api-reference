# Starshipit: Native API Reference

A consolidated summary of Starshipit's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://api-docs.starshipit.com/
- **API base URL:** `https://api.starshipit.com/api`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required
- **Subscription Key:** `subscriptionKey` · required · Subscription key from Starshipit Settings > API

Send these headers with each API request:

```http
StarShipIT-Api-Key: <apiKey>
Ocp-Apim-Subscription-Key: <subscriptionKey>
```

[Official authentication documentation](https://api-docs.starshipit.com/#getting-started)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

The total page count is read from `totalPages`. The current page number is read from `pageNumber`.

## Pagination

Use `page_size` in the query string to set the page size (default 50). Use `page_number` in the query string to choose the page; numbering starts at 1.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Address](actions/add-address.md) | `POST /addressbook/` | [docs](https://api-docs.starshipit.com/#f577d747-7227-432f-bbc2-d9e2db08578f) |
| [Add Product](actions/add-product.md) | `POST /products` | [docs](https://api-docs.starshipit.com/#8cfbd1b2-bd08-4cec-966f-7104cc147aee) |
| [Archive Order](actions/archive-order.md) | `POST /orders/archive` | [docs](https://api-docs.starshipit.com/#011a5cbf-56e3-4e89-b572-18e165e1a861) |
| [Assign Orders](actions/assign-orders.md) | `POST /orders/assign` | [docs](https://api-docs.starshipit.com/#2c72d243-06bb-4e98-8489-2608e47ea6e2) |
| [Batch Update Orders](actions/batch-update-orders.md) | `PUT /orders/batchupdate` | [docs](https://api-docs.starshipit.com/#8cb8c76d-16e0-4465-b07c-8355d5c012af) |
| [Clone Shipment](actions/clone-shipment.md) | `POST /orders/shipment/clone` | [docs](https://api-docs.starshipit.com/#83579b84-5333-4693-93d3-85d6b52f8e5b) |
| [Create Order](actions/create-order.md) | `POST /orders` | [docs](https://api-docs.starshipit.com/#abcadf5c-9793-47b3-a2cb-d650c666d84d) |
| [Create Orders](actions/create-orders.md) | `POST /orders/import` | [docs](https://api-docs.starshipit.com/#b90251d2-1d1c-47b1-ac07-eeeb21cade7b) |
| [Create Tracking Only Order](actions/create-tracking-only-order.md) | `POST /orders/shipped` | [docs](https://api-docs.starshipit.com/#a54f16e9-bf62-4041-b66e-4c4dd3da3250) |
| [Delete Address](actions/delete-address.md) | `POST /addressbook/delete` | [docs](https://api-docs.starshipit.com/#0cd0b1b0-7ba4-4da3-8c94-67cb4e020a6d) |
| [Delete Order](actions/delete-order.md) | `DELETE /orders/delete` | [docs](https://api-docs.starshipit.com/#c96bed4f-3a89-4e97-abaa-b1775cc7c5a7) |
| [Delete Product or All Products](actions/delete-product-or-all-products.md) | `DELETE /products/delete` | [docs](https://api-docs.starshipit.com/#5edb43f1-432b-4d1a-bb31-e05db0c879e3) |
| [Delivery Services](actions/delivery-services.md) | `POST /deliveryservices` | [docs](https://api-docs.starshipit.com/#11419b42-fcda-4cf6-b5e4-d572ba69147f) |
| [Get Order(s)](actions/get-order-s.md) | `GET /orders` | [docs](https://api-docs.starshipit.com/#0aef707f-e2f5-493a-a382-8235c00c9c18) |
| [Get Rates](actions/get-rates.md) | `POST /rates` | [docs](https://api-docs.starshipit.com/#03ce0c71-af60-4e3a-a967-451515dea9f6) |
| [Get Tracking Details](actions/get-tracking-details.md) | `GET /track` | [docs](https://api-docs.starshipit.com/#a655a3b4-ea39-42c4-acb4-d868ad40dc47) |
| [List Filtered Addresses](actions/list-filtered-addresses.md) | `GET /addressbook/filtered` | [docs](https://api-docs.starshipit.com/#4f93a04a-c4db-40bf-86d5-f4f8fd3fb265) |
| [List Manifest Files](actions/list-manifest-files.md) | `GET /manifests/files/` | [docs](https://api-docs.starshipit.com/#b6ca5673-49e9-4411-9281-4926b592466f) |
| [List Manifests](actions/list-manifests.md) | `GET /manifests` | [docs](https://api-docs.starshipit.com/#4961ecec-9175-4e55-ac4d-06cb0567c8ab) |
| [List Orders (Delivered)](actions/list-orders-delivered.md) | `GET /orders/delivered` | [docs](https://api-docs.starshipit.com/#57dda852-bab7-4c19-aefa-de756be7b46e) |
| [List Orders (Printed or Unmanifested)](actions/list-orders-printed-or-unmanifested.md) | `GET /orders/shipments` | [docs](https://api-docs.starshipit.com/#bc249299-e979-4003-becc-27ba61dcf214) |
| [List Orders (Shipped)](actions/list-orders-shipped.md) | `GET /orders/shipped` | [docs](https://api-docs.starshipit.com/#abbdf631-21c8-472b-b2e7-b1b68b01f6d0) |
| [List Orders Summary](actions/list-orders-summary.md) | `GET /orders/summary` | [docs](https://api-docs.starshipit.com/#c1e28347-54b6-4224-bca7-449469790840) |
| [List Orders (Unshipped)](actions/list-orders-unshipped.md) | `GET /orders/unshipped` | [docs](https://api-docs.starshipit.com/#6dd10a47-8403-4c7e-9b3f-32bf9986d8f3) |
| [List Suggested Merges](actions/list-suggested-merges.md) | `GET /orders/mergeable` | [docs](https://api-docs.starshipit.com/#27f95247-808e-45da-b058-2f80cb7713bb) |
| [Manifest by Carrier](actions/manifest-by-carrier.md) | `POST /manifests/carrier` | [docs](https://api-docs.starshipit.com/#065e6dad-6023-4e30-84c6-27aa02bb9211) |
| [Manifest Orders (Orders)](actions/manifest-orders-orders.md) | `POST /orders/manifest` | [docs](https://api-docs.starshipit.com/#4774c2b5-22a9-41ba-848c-fc0b872b1a39) |
| [Manifest Orders (Shipments)](actions/manifest-orders-shipments.md) | `POST /manifests/shipments` | [docs](https://api-docs.starshipit.com/#adc9e882-abfd-4488-b0c9-c1119591bdd6) |
| [Merge Orders](actions/merge-orders.md) | `POST /orders/merge` | [docs](https://api-docs.starshipit.com/#589357dc-f95d-4ac6-a54f-0ddb7d84b1fc) |
| [Print Label](actions/print-label.md) | `POST /orders/shipment` | [docs](https://api-docs.starshipit.com/#b6bc3576-a43f-4992-86d8-8fdf57f872f6) |
| [Print Labels](actions/print-labels.md) | `POST /orders/shipments` | [docs](https://api-docs.starshipit.com/#21741468-85a4-4dbb-b11c-1fe582fd54ce) |
| [Print Packing Slips](actions/print-packing-slips.md) | `POST /orders/packingslips` | [docs](https://api-docs.starshipit.com/#7855410a-b944-4888-a5bc-1054ca505d43) |
| [Replace Shipment](actions/replace-shipment.md) | `POST /orders/shipment/replace` | [docs](https://api-docs.starshipit.com/#3645a29f-5b34-4763-af4d-94fb6c34e649) |
| [Restore Order](actions/restore-order.md) | `POST /orders/restore` | [docs](https://api-docs.starshipit.com/#7894393b-a88e-41b3-af36-88a257d50c67) |
| [Search Orders](actions/search-orders.md) | `GET /orders/search` | [docs](https://api-docs.starshipit.com/#7615c4c5-893b-4085-aa67-5d1d34297654) |
| [Search Products](actions/search-products.md) | `GET /products` | [docs](https://api-docs.starshipit.com/#ccf0f10f-e370-45c0-ba5c-13bfaac80ca6) |
| [Update Address](actions/update-address.md) | `POST /addressbook/update` | [docs](https://api-docs.starshipit.com/#4ff9ae6f-fadb-4c50-9087-467c2e336f93) |
| [Update Order](actions/update-order.md) | `PUT /orders` | [docs](https://api-docs.starshipit.com/#fffefde7-2198-4e38-ae33-283792fd8321) |
| [Update Orders](actions/update-orders.md) | `PUT /orders/update` | [docs](https://api-docs.starshipit.com/#d3b7fa54-1fb9-46c9-9c3b-7fde0df4134e) |
| [Update Product](actions/update-product.md) | `PUT /products/update` | [docs](https://api-docs.starshipit.com/#9101a9d7-91b1-492c-b7ad-5f92f80bbfd7) |

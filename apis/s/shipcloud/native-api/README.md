# Shipcloud: Native API Reference

A consolidated summary of Shipcloud's API configuration and 33 documented operations, with links to official documentation.

- **Official docs:** https://developers.shipcloud.io/reference/
- **OpenAPI specification:** https://developers.shipcloud.io/downloads/api/oai/shipcloud_v1_oai3.json
- **API base URL:** `https://api.shipcloud.io/v1`

## Authentication

### Basic Auth

Use your Shipcloud API key as the username and leave the password blank.

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

[Official authentication documentation](https://developers.shipcloud.io/concepts/)

## Endpoints (33 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Address](actions/create-address.md) | `POST /addresses` | [docs](https://developers.shipcloud.io/swagger-ui/#/default/post_addresses) |
| [Create Manifest](actions/create-manifest.md) | `POST /manifests` | [docs](https://developers.shipcloud.io/swagger-ui/#/default/post_manifests) |
| [Create Order](actions/create-order.md) | `POST /orders` | [docs](https://developers.shipcloud.io/swagger-ui/#/default/post_orders) |
| [Create Pickup Request](actions/create-pickup-request.md) | `POST /pickup_requests` | [docs](https://developers.shipcloud.io/swagger-ui/#/default/post_pickup_requests) |
| [Create Shipment](actions/create-shipment.md) | `POST /shipments` | [docs](https://developers.shipcloud.io/swagger-ui/#/default/post_shipments) |
| [Create Shipment Document](actions/create-shipment-document.md) | `POST /shipments/:shipmentId/shipment_documents` | [docs](https://developers.shipcloud.io/swagger-ui/#/default/post_shipments__shipment_id__shipment_documents) |
| [Create Shipment Quote](actions/create-shipment-quote.md) | `POST /shipment_quotes` | [docs](https://developers.shipcloud.io/swagger-ui/#/default/post_shipment_quotes) |
| [Create Tracker](actions/create-tracker.md) | `POST /trackers` | [docs](https://developers.shipcloud.io/swagger-ui/#/default/post_trackers) |
| [Create Webhook](actions/create-webhook.md) | `POST /webhooks` | [docs](https://developers.shipcloud.io/swagger-ui/#/default/post_webhooks) |
| [Delete Shipment](actions/delete-shipment.md) | `DELETE /shipments/:id` | [docs](https://developers.shipcloud.io/swagger-ui/#/default/delete_shipments__id_) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /webhooks/:id` | [docs](https://developers.shipcloud.io/swagger-ui/#/default/delete_webhooks__id_) |
| [Get Address](actions/get-address.md) | `GET /addresses/:id` | [docs](https://developers.shipcloud.io/swagger-ui/#/default/get_addresses__id_) |
| [Get Current User](actions/get-current-user.md) | `GET /me` | [docs](https://developers.shipcloud.io/swagger-ui/#/default/get_me) |
| [Get Default Returns Address](actions/get-default-returns-address.md) | `GET /default_returns_address` | [docs](https://developers.shipcloud.io/swagger-ui/#/default/get_default_returns_address) |
| [Get Default Shipping Address](actions/get-default-shipping-address.md) | `GET /default_shipping_address` | [docs](https://developers.shipcloud.io/swagger-ui/#/default/get_default_shipping_address) |
| [Get Invoice Address](actions/get-invoice-address.md) | `GET /invoice_address` | [docs](https://developers.shipcloud.io/swagger-ui/#/default/get_invoice_address) |
| [Get Manifest](actions/get-manifest.md) | `GET /manifests/:id` | [docs](https://developers.shipcloud.io/swagger-ui/#/default/get_manifests__id_) |
| [Get Order](actions/get-order.md) | `GET /orders/:id` | [docs](https://developers.shipcloud.io/swagger-ui/#/default/get_orders__id_) |
| [Get Pickup Request](actions/get-pickup-request.md) | `GET /pickup_requests/:id` | [docs](https://developers.shipcloud.io/swagger-ui/#/default/get_pickup_requests__id_) |
| [Get Shipment](actions/get-shipment.md) | `GET /shipments/:id` | [docs](https://developers.shipcloud.io/swagger-ui/#/default/get_shipments__id_) |
| [Get Shipment Document](actions/get-shipment-document.md) | `GET /shipments/:shipmentId/shipment_documents/:shipmentDocumentId` | [docs](https://developers.shipcloud.io/swagger-ui/#/default/get_shipments__shipment_id__shipment_documents__shipment_document_id_) |
| [Get Tracker](actions/get-tracker.md) | `GET /trackers/:id` | [docs](https://developers.shipcloud.io/swagger-ui/#/default/get_trackers__id_) |
| [Get Webhook](actions/get-webhook.md) | `GET /webhooks/:id` | [docs](https://developers.shipcloud.io/swagger-ui/#/default/get_webhooks__id_) |
| [List Addresses](actions/list-addresses.md) | `GET /addresses` | [docs](https://developers.shipcloud.io/swagger-ui/#/default/get_addresses) |
| [List Carriers](actions/list-carriers.md) | `GET /carriers` | [docs](https://developers.shipcloud.io/swagger-ui/#/default/get_carriers) |
| [List Orders](actions/list-orders.md) | `GET /orders` | [docs](https://developers.shipcloud.io/swagger-ui/#/default/get_orders) |
| [List Pickup Requests](actions/list-pickup-requests.md) | `GET /pickup_requests` | [docs](https://developers.shipcloud.io/swagger-ui/#/default/get_pickup_requests) |
| [List Shipment Documents](actions/list-shipment-documents.md) | `GET /shipments/:shipmentId/shipment_documents` | [docs](https://developers.shipcloud.io/swagger-ui/#/default/get_shipments__shipment_id__shipment_documents) |
| [List Shipments](actions/list-shipments.md) | `GET /shipments` | [docs](https://developers.shipcloud.io/swagger-ui/#/default/get_shipments) |
| [List Trackers](actions/list-trackers.md) | `GET /trackers` | [docs](https://developers.shipcloud.io/swagger-ui/#/default/get_trackers) |
| [List Webhooks](actions/list-webhooks.md) | `GET /webhooks` | [docs](https://developers.shipcloud.io/swagger-ui/#/default/get_webhooks) |
| [Search Pickup Dropoff Locations](actions/search-pickup-dropoff-locations.md) | `GET /pickup_dropoff_locations` | [docs](https://developers.shipcloud.io/swagger-ui/#/default/get_pickup_dropoff_locations) |
| [Update Shipment](actions/update-shipment.md) | `PUT /shipments/:id` | [docs](https://developers.shipcloud.io/swagger-ui/#/default/put_shipments__id_) |

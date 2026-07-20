# <img src="https://images.mindcloud.co/apps/icons/printify-icon_1776087406957.png" alt="Printify logo" width="28" height="28"> Printify: Universal API

Connect Printify personal access tokens to manage shops, catalog blueprints, products, orders, uploads, print providers, and webhooks through the Printify REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/printify/latest
- **Category:** Commerce
- **Actions:** 35
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://printify.com/
- **Vendor API docs:** https://developers.printify.com/API-Doc-RREdits.html/1000

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Shops](actions/list-shops.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/printify/latest/actions/list-shops?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (35)

### Blueprint

| Action | Method | Description |
| --- | --- | --- |
| [Get Blueprint](actions/get-blueprint.md) | GET | Retrieves a blueprint from Printify. |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Order](actions/cancel-order.md) | PUT | Cancels an unpaid order in Printify. |
| [Send Order To Production](actions/send-order-to-production.md) | PUT | Sends an order to production in Printify. |
| [Submit Express Order](actions/submit-express-order.md) | POST | Submits a Printify Express order. |
| [Submit Order](actions/submit-order.md) | POST | Submits an order to Printify. |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [Create Product](actions/create-product.md) | POST | Creates a product in Printify. |
| [Delete Product](actions/delete-product.md) | DELETE | Deletes a product from Printify. |
| [Publish Product](actions/publish-product.md) | PUT | Publishes a product in Printify. |
| [Set Product Publish Failed](actions/set-product-publish-failed.md) | PUT | Marks a product publish as failed in Printify. |
| [Set Product Publish Succeeded](actions/set-product-publish-succeeded.md) | PUT | Marks a product publish as succeeded in Printify. |
| [Unpublish Product](actions/unpublish-product.md) | PUT | Unpublishes a product in Printify. |
| [Update Product](actions/update-product.md) | PUT | Updates a product in Printify. |

### Shippingquote

| Action | Method | Description |
| --- | --- | --- |
| [Calculate Order Shipping](actions/calculate-order-shipping.md) | GET | Calculates order shipping in Printify. |

### Shop

| Action | Method | Description |
| --- | --- | --- |
| [Disconnect Shop Connection](actions/disconnect-shop-connection.md) | DELETE | Disconnects a Printify shop connection. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Get Blueprint Shipping](actions/get-blueprint-shipping.md) | GET | Retrieves blueprint shipping details from Printify. |
| [Get Order](actions/get-order.md) | GET | Retrieves an order from Printify. |
| [Get Print Provider](actions/get-print-provider.md) | GET | Retrieves a print provider from Printify. |
| [Get Product](actions/get-product.md) | GET | Retrieves a product from Printify. |
| [Get Product GPSR](actions/get-product-gpsr.md) | GET | Retrieves a product's GPSR information from Printify. |
| [Get Upload](actions/get-upload.md) | GET | Retrieves an upload from Printify. |
| [List Blueprint Print Providers](actions/list-blueprint-print-providers.md) | GET | Retrieves blueprint print providers from Printify. |
| [List Blueprint Variants](actions/list-blueprint-variants.md) | GET | Retrieves blueprint variants from Printify. |
| [List Blueprints](actions/list-blueprints.md) | GET | Retrieves blueprints from Printify. |
| [List Orders](actions/list-orders.md) | GET | Retrieves orders from a Printify shop. |
| [List Print Providers](actions/list-print-providers.md) | GET | Retrieves print providers from Printify. |
| [List Products](actions/list-products.md) | GET | Retrieves products from a Printify shop. |
| [List Shops](actions/list-shops.md) | GET | Retrieves shops from Printify. |
| [List Uploads](actions/list-uploads.md) | GET | Retrieves uploads from Printify. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhooks from a Printify shop. |

### Upload

| Action | Method | Description |
| --- | --- | --- |
| [Archive Upload](actions/archive-upload.md) | PUT | Archives an uploaded image in Printify. |
| [Upload Image](actions/upload-image.md) | POST | Uploads an image to Printify. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a webhook in Printify. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes a webhook from Printify. |
| [Update Webhook](actions/update-webhook.md) | PUT | Updates a webhook in Printify. |

### Webhooksimulation

| Action | Method | Description |
| --- | --- | --- |
| [Simulate Webhook](actions/simulate-webhook.md) | PUT | Simulates a webhook in Printify. |


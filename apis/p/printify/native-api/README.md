# Printify: Native API Reference

A consolidated summary of Printify's API configuration and 35 documented operations, with links to official documentation.

- **Official docs:** https://developers.printify.com/API-Doc-RREdits.html/1000
- **OpenAPI specification:** https://developers.printify.com/API-Doc-RREdits.html/openapi.json
- **API base URL:** `https://api.printify.com/v1/`

## Authentication

### Personal Access Token

Use a Printify personal access token. Printify sends API requests with Authorization: Bearer <token>.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developers.printify.com/API-Doc-RREdits.html/1000)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `User-Agent` | `MindCloud` |

## Pagination

Use `limit` in the query string to set the page size (default 10; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (35 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Archive Upload](actions/archive-upload.md) | `POST /uploads/:image_id/archive.json` | [docs](https://developers.printify.com/API-Doc-RREdits.html/1000) |
| [Calculate Order Shipping](actions/calculate-order-shipping.md) | `POST /shops/:shop_id/orders/shipping.json` | [docs](https://developers.printify.com/API-Doc-RREdits.html/1000) |
| [Cancel Order](actions/cancel-order.md) | `POST /shops/:shop_id/orders/:order_id/cancel.json` | [docs](https://developers.printify.com/API-Doc-RREdits.html/1000) |
| [Create Product](actions/create-product.md) | `POST /shops/:shop_id/products.json` | [docs](https://developers.printify.com/API-Doc-RREdits.html/1000) |
| [Create Webhook](actions/create-webhook.md) | `POST /shops/:shop_id/webhooks.json` | [docs](https://developers.printify.com/API-Doc-RREdits.html/1000) |
| [Delete Product](actions/delete-product.md) | `DELETE /shops/:shop_id/products/:product_id.json` | [docs](https://developers.printify.com/API-Doc-RREdits.html/1000) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /shops/:shop_id/webhooks/:webhook_id.json` | [docs](https://developers.printify.com/API-Doc-RREdits.html/1000) |
| [Disconnect Shop Connection](actions/disconnect-shop-connection.md) | `DELETE /shops/:shop_id/connection.json` | [docs](https://developers.printify.com/API-Doc-RREdits.html/1000) |
| [Get Blueprint](actions/get-blueprint.md) | `GET /catalog/blueprints/:blueprint_id.json` | [docs](https://developers.printify.com/API-Doc-RREdits.html/1000) |
| [Get Blueprint Shipping](actions/get-blueprint-shipping.md) | `GET /catalog/blueprints/:blueprint_id/print_providers/:print_provider_id/shipping.json` | [docs](https://developers.printify.com/API-Doc-RREdits.html/1000) |
| [Get Order](actions/get-order.md) | `GET /shops/:shop_id/orders/:order_id.json` | [docs](https://developers.printify.com/API-Doc-RREdits.html/1000) |
| [Get Print Provider](actions/get-print-provider.md) | `GET /catalog/print_providers/:print_provider_id.json` | [docs](https://developers.printify.com/API-Doc-RREdits.html/1000) |
| [Get Product](actions/get-product.md) | `GET /shops/:shop_id/products/:product_id.json` | [docs](https://developers.printify.com/API-Doc-RREdits.html/1000) |
| [Get Product GPSR](actions/get-product-gpsr.md) | `GET /shops/:shop_id/products/:product_id/gpsr.json` | [docs](https://developers.printify.com/API-Doc-RREdits.html/1000) |
| [Get Upload](actions/get-upload.md) | `GET /uploads/:image_id.json` | [docs](https://developers.printify.com/API-Doc-RREdits.html/1000) |
| [List Blueprint Print Providers](actions/list-blueprint-print-providers.md) | `GET /catalog/blueprints/:blueprint_id/print_providers.json` | [docs](https://developers.printify.com/API-Doc-RREdits.html/1000) |
| [List Blueprint Variants](actions/list-blueprint-variants.md) | `GET /catalog/blueprints/:blueprint_id/print_providers/:print_provider_id/variants.json` | [docs](https://developers.printify.com/API-Doc-RREdits.html/1000) |
| [List Blueprints](actions/list-blueprints.md) | `GET /catalog/blueprints.json` | [docs](https://developers.printify.com/API-Doc-RREdits.html/1000) |
| [List Orders](actions/list-orders.md) | `GET /shops/:shop_id/orders.json` | [docs](https://developers.printify.com/API-Doc-RREdits.html/1000) |
| [List Print Providers](actions/list-print-providers.md) | `GET /catalog/print_providers.json` | [docs](https://developers.printify.com/API-Doc-RREdits.html/1000) |
| [List Products](actions/list-products.md) | `GET /shops/:shop_id/products.json` | [docs](https://developers.printify.com/API-Doc-RREdits.html/1000) |
| [List Shops](actions/list-shops.md) | `GET /shops.json` | [docs](https://developers.printify.com/API-Doc-RREdits.html/1000) |
| [List Uploads](actions/list-uploads.md) | `GET /uploads.json` | [docs](https://developers.printify.com/API-Doc-RREdits.html/1000) |
| [List Webhooks](actions/list-webhooks.md) | `GET /shops/:shop_id/webhooks.json` | [docs](https://developers.printify.com/API-Doc-RREdits.html/1000) |
| [Publish Product](actions/publish-product.md) | `POST /shops/:shop_id/products/:product_id/publish.json` | [docs](https://developers.printify.com/API-Doc-RREdits.html/1000) |
| [Send Order To Production](actions/send-order-to-production.md) | `POST /shops/:shop_id/orders/:order_id/send_to_production.json` | [docs](https://developers.printify.com/API-Doc-RREdits.html/1000) |
| [Set Product Publish Failed](actions/set-product-publish-failed.md) | `POST /shops/:shop_id/products/:product_id/publishing_failed.json` | [docs](https://developers.printify.com/API-Doc-RREdits.html/1000) |
| [Set Product Publish Succeeded](actions/set-product-publish-succeeded.md) | `POST /shops/:shop_id/products/:product_id/publishing_succeeded.json` | [docs](https://developers.printify.com/API-Doc-RREdits.html/1000) |
| [Simulate Webhook](actions/simulate-webhook.md) | `POST /shops/:shop_id/webhooks/:webhook_id/simulate` | [docs](https://developers.printify.com/API-Doc-RREdits.html/1000) |
| [Submit Express Order](actions/submit-express-order.md) | `POST /shops/:shop_id/orders/express.json` | [docs](https://developers.printify.com/API-Doc-RREdits.html/1000) |
| [Submit Order](actions/submit-order.md) | `POST /shops/:shop_id/orders.json` | [docs](https://developers.printify.com/API-Doc-RREdits.html/1000) |
| [Unpublish Product](actions/unpublish-product.md) | `POST /shops/:shop_id/products/:product_id/unpublish.json` | [docs](https://developers.printify.com/API-Doc-RREdits.html/1000) |
| [Update Product](actions/update-product.md) | `PUT /shops/:shop_id/products/:product_id.json` | [docs](https://developers.printify.com/API-Doc-RREdits.html/1000) |
| [Update Webhook](actions/update-webhook.md) | `PUT /shops/:shop_id/webhooks/:webhook_id.json` | [docs](https://developers.printify.com/API-Doc-RREdits.html/1000) |
| [Upload Image](actions/upload-image.md) | `POST /uploads/images.json` | [docs](https://developers.printify.com/API-Doc-RREdits.html/1000) |

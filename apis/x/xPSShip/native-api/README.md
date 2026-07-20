# XPS Ship: Native API Reference

A consolidated summary of XPS Ship's API configuration and 12 documented operations, with links to official documentation.

- **Official docs:** https://xpsshipper.com/restapi/docs/v1-ecommerce/endpoints/overview/
- **API base URL:** `https://xpsshipper.com`

## Authentication

### XPS Ship API key

Uses the XPS Ship eCommerce API Authorization header with the provider-specific RSIS prefix.

### Credentials

- **API key:** `apiKey` · required · XPS Ship API key used in the Authorization header with the RSIS prefix.
- **Customer ID:** `customerId` · required · XPS Ship Customer ID used in customer-scoped REST paths.

[Official authentication documentation](https://xpsshipper.com/restapi/docs/v1-ecommerce/endpoints/overview/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `limit` in the query string to set the page size (default 100; accepted range 1–100).

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 500 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (12 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Assign Tags to Order](actions/assign-tags-to-order.md) | `POST /restapi/v1/customers/:customerId/integrations/:integrationId/orders/:orderId/assign-tags` | [docs](https://xpsshipper.com/restapi/docs/v1-ecommerce/endpoints/assign-tags-to-order/) |
| [Create Quote](actions/create-quote.md) | `POST /restapi/v1/customers/:customerId/quote` | [docs](https://xpsshipper.com/restapi/docs/v1-ecommerce/endpoints/quote/) |
| [Delete Order](actions/delete-order.md) | `DELETE /restapi/v1/customers/:customerId/integrations/:integrationId/orders/:orderId` | [docs](https://xpsshipper.com/restapi/docs/v1-ecommerce/endpoints/delete-order/) |
| [List Integrated Quoting Options](actions/list-integrated-quoting-options.md) | `GET /restapi/v1/customers/:customerId/integratedQuotingOptions` | [docs](https://xpsshipper.com/restapi/docs/v1-ecommerce/endpoints/list-integrated-quoting-options/) |
| [List Order Tags](actions/list-order-tags.md) | `GET /restapi/v1/customers/:customerId/list-tags` | [docs](https://xpsshipper.com/restapi/docs/v1-ecommerce/endpoints/list-order-tags/) |
| [List Services](actions/list-services.md) | `GET /restapi/v1/customers/:customerId/services` | [docs](https://xpsshipper.com/restapi/docs/v1-ecommerce/endpoints/list-services/) |
| [Put Order](actions/put-order.md) | `PUT /restapi/v1/customers/:customerId/integrations/:integrationId/orders/:orderId` | [docs](https://xpsshipper.com/restapi/docs/v1-ecommerce/endpoints/put-order/) |
| [Retrieve Shipment](actions/retrieve-shipment.md) | `GET /restapi/v1/customers/:customerId/shipments/:bookNumber` | [docs](https://xpsshipper.com/restapi/docs/v1-ecommerce/endpoints/retrieve-shipment/) |
| [Retrieve Shipments](actions/retrieve-shipments.md) | `GET /restapi/v1/customers/:customerId/shipments` | [docs](https://xpsshipper.com/restapi/docs/v1-ecommerce/endpoints/retrieve-shipments/) |
| [Retrieve Shipping Label](actions/retrieve-shipping-label.md) | `GET /restapi/v1/customers/:customerId/shipments/:bookNumber/label/:labelImageFormat` | [docs](https://xpsshipper.com/restapi/docs/v1-ecommerce/endpoints/retrieve-shipping-label/) |
| [Search Shipments](actions/search-shipments.md) | `POST /restapi/v1/customers/:customerId/searchShipments` | [docs](https://xpsshipper.com/restapi/docs/v1-ecommerce/endpoints/search-shipments/) |
| [Unassign Tags from Order](actions/unassign-tags-from-order.md) | `POST /restapi/v1/customers/:customerId/integrations/:integrationId/orders/:orderId/unassign-tags` | [docs](https://xpsshipper.com/restapi/docs/v1-ecommerce/endpoints/unassign-tags-from-order/) |

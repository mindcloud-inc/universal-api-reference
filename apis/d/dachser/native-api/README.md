# Dachser: Native API Reference

A consolidated summary of Dachser's API configuration and 19 documented operations, with links to official documentation.

- **Official docs:** https://api-portal.dachser.com/bi.b2b.portal/api
- **OpenAPI specification:** https://api-portal.dachser.com/bi.b2b.portal/swagger-ui/transportorder.yaml
- **API base URL:** `https://api-gateway.dachser.com/`

## Authentication

### API Key

Use a DACHSER API token generated or subscribed through the DACHSER API Portal. The token is sent to DACHSER as the X-API-Key header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://api-portal.dachser.com/bi.b2b.portal/api/getting-started)

## API conventions

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (19 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Labels](actions/create-labels.md) | `POST /rest/v2/labels` | [docs](https://api-portal.dachser.com/bi.b2b.portal/api/library/label) |
| [Create Quotation](actions/create-quotation.md) | `POST /rest/v2/quotations` | [docs](https://api-portal.dachser.com/bi.b2b.portal/api/library/quotation) |
| [Create SSCC Codes](actions/create-sscc-codes.md) | `POST /rest/v2/ssccs` | [docs](https://api-portal.dachser.com/bi.b2b.portal/api/library/sscc) |
| [Create Transport Order](actions/create-transport-order.md) | `POST /rest/v2/transportorders/{basket}` | [docs](https://api-portal.dachser.com/bi.b2b.portal/api/library/transportorder) |
| [Delete Transport Order](actions/delete-transport-order.md) | `DELETE /rest/v2/transportorders/{id}` | [docs](https://api-portal.dachser.com/bi.b2b.portal/api/library/transportorder) |
| [Download Transfer Lists](actions/download-transfer-lists.md) | `GET /rest/v2/transferlists/{orderdate}` | [docs](https://api-portal.dachser.com/bi.b2b.portal/api/library/transportorder) |
| [Get Delivery Notes](actions/get-delivery-notes.md) | `GET /rest/v2/deliverynotes` | [docs](https://api-portal.dachser.com/bi.b2b.portal/api/library/deliverynotes) |
| [Get Delivery Order Status](actions/get-delivery-order-status.md) | `GET /rest/v2/deliveryorderstatus` | [docs](https://api-portal.dachser.com/bi.b2b.portal/api/library/deliveryorderstatus) |
| [Get Freight Costs](actions/get-freight-costs.md) | `GET /rest/v2/freightcosts` | [docs](https://api-portal.dachser.com/bi.b2b.portal/api/library/freightcosts) |
| [Get Incoming Goods Documents](actions/get-incoming-goods-documents.md) | `GET /rest/v2/incominggoodsdocuments` | [docs](https://api-portal.dachser.com/bi.b2b.portal/api/library/incominggoodsdocuments) |
| [Get Proofs Of Delivery](actions/get-proofs-of-delivery.md) | `GET /rest/v2/pods` | [docs](https://api-portal.dachser.com/bi.b2b.portal/api/library/pod) |
| [Get Routing](actions/get-routing.md) | `GET /rest/v2/routings` | [docs](https://api-portal.dachser.com/bi.b2b.portal/api/library/routing) |
| [Get Shipment History](actions/get-shipment-history.md) | `GET /rest/v2/shipmenthistory` | [docs](https://api-portal.dachser.com/bi.b2b.portal/api/library/shipmenthistory) |
| [Get Shipment Status](actions/get-shipment-status.md) | `GET /rest/v2/shipmentstatus` | [docs](https://api-portal.dachser.com/bi.b2b.portal/api/library/shipmentstatus) |
| [Get Stock](actions/get-stock.md) | `GET /rest/v2/stocks` | [docs](https://api-portal.dachser.com/bi.b2b.portal/api/library/stock) |
| [Get Transport Order Labels](actions/get-transport-order-labels.md) | `POST /rest/v2/transportorders/{id}/labels` | [docs](https://api-portal.dachser.com/bi.b2b.portal/api/library/transportorder) |
| [List Transport Orders](actions/list-transport-orders.md) | `GET /rest/v2/transportorders` | [docs](https://api-portal.dachser.com/bi.b2b.portal/api/library/transportorder) |
| [List Transport Orders By Basket](actions/list-transport-orders-by-basket.md) | `GET /rest/v2/transportorders/{basket}` | [docs](https://api-portal.dachser.com/bi.b2b.portal/api/library/transportorder) |
| [Send Transport Order](actions/send-transport-order.md) | `POST /rest/v2/transportorders/{id}/send` | [docs](https://api-portal.dachser.com/bi.b2b.portal/api/library/transportorder) |

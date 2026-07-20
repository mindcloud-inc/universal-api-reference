# Billit: Native API Reference

A consolidated summary of Billit's API configuration and 13 documented operations, with links to official documentation.

- **Official docs:** https://docs.billit.be/reference
- **OpenAPI specification:** https://docs.billit.be/reference/account_getaccountinformation-1
- **API base URL:** `https://api.sandbox.billit.be`

## Authentication

### API Key

Authenticate with Billit API key plus Party ID headers.

### Credentials

- **API Key:** `apiKey` · required
- **Party ID:** `partyId` · required · Billit PartyID for the selected company and environment.

Send these headers with each API request:

```http
ApiKey: <apiKey>
PartyID: <partyId>
```

[Official authentication documentation](https://docs.billit.be/docs/partyid-and-key)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (13 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Party](actions/create-party.md) | `POST /v1/parties` | [docs](https://docs.billit.be/reference/party_postparty-1) |
| [Create Sales Invoice](actions/create-sales-invoice.md) | `POST /v1/orders` | [docs](https://docs.billit.be/reference/order_postorders-1) |
| [Delete Order](actions/delete-order.md) | `DELETE /v1/orders/:orderID` | [docs](https://docs.billit.be/reference/order_deleteorder-1) |
| [Get Account Information](actions/get-account-information.md) | `GET /v1/account/accountInformation` | [docs](https://docs.billit.be/reference/account_getaccountinformation-1) |
| [Get Next Invoice Sequence](actions/get-next-invoice-sequence.md) | `POST /v1/account/sequences` | [docs](https://docs.billit.be/reference/account_postsequences-1) |
| [Get Order](actions/get-order.md) | `GET /v1/orders/:orderID` | [docs](https://docs.billit.be/reference/order_getorders_orderid) |
| [Get Party](actions/get-party.md) | `GET /v1/parties/:partyID` | [docs](https://docs.billit.be/reference/party_getparty-1) |
| [Get Product](actions/get-product.md) | `GET /v1/products/:productID` | [docs](https://docs.billit.be/reference/product_getproduct-1) |
| [List Orders](actions/list-orders.md) | `GET /v1/orders` | [docs](https://docs.billit.be/reference/order_getorders-1) |
| [List Parties](actions/list-parties.md) | `GET /v1/parties` | [docs](https://docs.billit.be/reference/party_getparties-1) |
| [List Products](actions/list-products.md) | `GET /v1/products` | [docs](https://docs.billit.be/reference/product_getproducts-1) |
| [Update Order Export Status](actions/update-order-export-status.md) | `PATCH /v1/orders/:orderID` | [docs](https://docs.billit.be/reference/order_patchorders-1) |
| [Update Party](actions/update-party.md) | `PATCH /v1/parties/:partyID` | [docs](https://docs.billit.be/reference/party_patchparties-1) |

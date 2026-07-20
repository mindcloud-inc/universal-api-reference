# eGestor: Native API Reference

A consolidated summary of eGestor's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://egestor.docs.apiary.io/
- **API base URL:** `https://api.egestor.com.br/api/v1`

## Authentication

### Bearer Access Token

Use the returned eGestor access_token as the MindCloud API key value. The provider docs do not define a standard OAuth browser authorization flow, so bearer-token auth is the safest contract for now.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://egestor.docs.apiary.io/#group-autenticacao---oauth)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check Pix Status](actions/check-pix-status.md) | `GET /pix/:codigo/consultarSituacao` | [docs](https://github.com/eGestor/documentacao-api/blob/master/apiary.apib#L4941) |
| [Create Contact](actions/create-contact.md) | `POST /contatos` | [docs](https://github.com/eGestor/documentacao-api/blob/master/apiary.apib#L270) |
| [Create Payable](actions/create-payable.md) | `POST /pagamentos` | [docs](https://github.com/eGestor/documentacao-api/blob/master/apiary.apib#L2838) |
| [Create Pix Charge](actions/create-pix-charge.md) | `POST /pix` | [docs](https://github.com/eGestor/documentacao-api/blob/master/apiary.apib#L4792) |
| [Create Product](actions/create-product.md) | `POST /produtos` | [docs](https://github.com/eGestor/documentacao-api/blob/master/apiary.apib#L898) |
| [Create Purchase](actions/create-purchase.md) | `POST /compras` | [docs](https://github.com/eGestor/documentacao-api/blob/master/apiary.apib#L3179) |
| [Create Receivable](actions/create-receivable.md) | `POST /recebimentos` | [docs](https://github.com/eGestor/documentacao-api/blob/master/apiary.apib#L2536) |
| [Create Sale](actions/create-sale.md) | `POST /vendas` | [docs](https://github.com/eGestor/documentacao-api/blob/master/apiary.apib#L3630) |
| [Create Service](actions/create-service.md) | `POST /servicos` | [docs](https://github.com/eGestor/documentacao-api/blob/master/apiary.apib#L1381) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /contatos/:codigo` | [docs](https://github.com/eGestor/documentacao-api/blob/master/apiary.apib#L582) |
| [Delete Product](actions/delete-product.md) | `DELETE /produtos/:codigo` | [docs](https://github.com/eGestor/documentacao-api/blob/master/apiary.apib#L1094) |
| [Delete Service](actions/delete-service.md) | `DELETE /servicos/:codigo` | [docs](https://github.com/eGestor/documentacao-api/blob/master/apiary.apib#L1536) |
| [Finalize Purchase](actions/finalize-purchase.md) | `GET /compras/:codigo/efetivar` | [docs](https://github.com/eGestor/documentacao-api/blob/master/apiary.apib#L3416) |
| [Generate Sale NFe](actions/generate-sale-n-fe.md) | `POST /vendas/:codigo/gerarNfe` | [docs](https://github.com/eGestor/documentacao-api/blob/master/apiary.apib#L4137) |
| [Get Company](actions/get-company.md) | `GET /empresa` | [docs](https://egestor.docs.apiary.io/#reference/recursos/empresa) |
| [Get Contact](actions/get-contact.md) | `GET /contatos/:codigo` | [docs](https://github.com/eGestor/documentacao-api/blob/master/apiary.apib#L384) |
| [Get Payable](actions/get-payable.md) | `GET /pagamentos/:codigo` | [docs](https://github.com/eGestor/documentacao-api/blob/master/apiary.apib#L2882) |
| [Get Pix Charge](actions/get-pix-charge.md) | `GET /pix/:codigo` | [docs](https://github.com/eGestor/documentacao-api/blob/master/apiary.apib#L4839) |
| [Get Product](actions/get-product.md) | `GET /produtos/:codigo` | [docs](https://github.com/eGestor/documentacao-api/blob/master/apiary.apib#L946) |
| [Get Purchase](actions/get-purchase.md) | `GET /compras/:codigo` | [docs](https://github.com/eGestor/documentacao-api/blob/master/apiary.apib#L3284) |
| [Get Receivable](actions/get-receivable.md) | `GET /recebimentos/:codigo` | [docs](https://github.com/eGestor/documentacao-api/blob/master/apiary.apib#L2582) |
| [Get Sale](actions/get-sale.md) | `GET /vendas/:codigo` | [docs](https://github.com/eGestor/documentacao-api/blob/master/apiary.apib#L3733) |
| [Get Service](actions/get-service.md) | `GET /servicos/:codigo` | [docs](https://github.com/eGestor/documentacao-api/blob/master/apiary.apib#L1416) |
| [List Contacts](actions/list-contacts.md) | `GET /contatos` | [docs](https://github.com/eGestor/documentacao-api/blob/master/apiary.apib#L201) |
| [List Payables](actions/list-payables.md) | `GET /pagamentos` | [docs](https://github.com/eGestor/documentacao-api/blob/master/apiary.apib#L2767) |
| [List Pix Charges](actions/list-pix-charges.md) | `GET /pix` | [docs](https://github.com/eGestor/documentacao-api/blob/master/apiary.apib#L4744) |
| [List Products](actions/list-products.md) | `GET /produtos` | [docs](https://github.com/eGestor/documentacao-api/blob/master/apiary.apib#L794) |
| [List Purchases](actions/list-purchases.md) | `GET /compras` | [docs](https://github.com/eGestor/documentacao-api/blob/master/apiary.apib#L3111) |
| [List Receivables](actions/list-receivables.md) | `GET /recebimentos` | [docs](https://github.com/eGestor/documentacao-api/blob/master/apiary.apib#L2457) |
| [List Sales](actions/list-sales.md) | `GET /vendas` | [docs](https://github.com/eGestor/documentacao-api/blob/master/apiary.apib#L3551) |
| [List Services](actions/list-services.md) | `GET /servicos` | [docs](https://github.com/eGestor/documentacao-api/blob/master/apiary.apib#L1340) |
| [Pay Payable](actions/pay-payable.md) | `PUT /pagamentos/:codigo/pagar` | [docs](https://github.com/eGestor/documentacao-api/blob/master/apiary.apib#L3049) |
| [Receive Receivable](actions/receive-receivable.md) | `PUT /recebimentos/:codigo/receber` | [docs](https://github.com/eGestor/documentacao-api/blob/master/apiary.apib#L2708) |
| [Reopen Purchase](actions/reopen-purchase.md) | `GET /compras/:codigo/reabrir` | [docs](https://github.com/eGestor/documentacao-api/blob/master/apiary.apib#L3445) |
| [Update Contact](actions/update-contact.md) | `PUT /contatos/:codigo` | [docs](https://github.com/eGestor/documentacao-api/blob/master/apiary.apib#L477) |
| [Update Payable](actions/update-payable.md) | `PUT /pagamentos/:codigo` | [docs](https://github.com/eGestor/documentacao-api/blob/master/apiary.apib#L3001) |
| [Update Product](actions/update-product.md) | `PUT /produtos/:codigo` | [docs](https://github.com/eGestor/documentacao-api/blob/master/apiary.apib#L1019) |
| [Update Receivable](actions/update-receivable.md) | `PUT /recebimentos/:codigo` | [docs](https://github.com/eGestor/documentacao-api/blob/master/apiary.apib#L2662) |
| [Update Sale](actions/update-sale.md) | `PUT /vendas/:codigo` | [docs](https://github.com/eGestor/documentacao-api/blob/master/apiary.apib#L3863) |
| [Update Service](actions/update-service.md) | `PUT /servicos/:codigo` | [docs](https://github.com/eGestor/documentacao-api/blob/master/apiary.apib#L1474) |

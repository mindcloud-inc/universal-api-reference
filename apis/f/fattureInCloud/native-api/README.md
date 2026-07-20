# Fatture in Cloud: Native API Reference

A consolidated summary of Fatture in Cloud's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://developers.fattureincloud.it/api-reference/
- **OpenAPI specification:** https://raw.githubusercontent.com/fattureincloud/openapi-fattureincloud/master/openapi.yaml
- **API base URL:** `https://api-v2.fattureincloud.it`

## Authentication

### OAuth 2.0

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://api-v2.fattureincloud.it/oauth/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://api-v2.fattureincloud.it/oauth/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `entity.clients:r entity.clients:a entity.suppliers:r entity.suppliers:a products:r products:a issued_documents.invoices:r issued_documents.invoices:a issued_documents.credit_notes:r issued_documents.credit_notes:a issued_documents.receipts:r issued_documents.receipts:a issued_documents.orders:r issued_documents.orders:a issued_documents.quotes:r issued_documents.quotes:a issued_documents.proformas:r issued_documents.proformas:a issued_documents.delivery_notes:r issued_documents.delivery_notes:a received_documents:r received_documents:a stock:r stock:a receipts:r receipts:a`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://api-v2.fattureincloud.it/oauth/token.

[Official authentication documentation](https://developers.fattureincloud.it/docs/authentication/code-flow/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `per_page` in the query string to set the page size (default 5; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `sort` in the query string. Prefix the field name to select its direction. Multiple sort fields can be combined.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Client](actions/create-client.md) | `POST /c/:company_id/entities/clients` | [docs](https://developers.fattureincloud.it/api-reference/#operation/createClient) |
| [Create Issued Document](actions/create-issued-document.md) | `POST /c/:company_id/issued_documents` | [docs](https://developers.fattureincloud.it/api-reference/#operation/createIssuedDocument) |
| [Create Product](actions/create-product.md) | `POST /c/:company_id/products` | [docs](https://developers.fattureincloud.it/api-reference/#operation/createProduct) |
| [Create Receipt](actions/create-receipt.md) | `POST /c/:company_id/receipts` | [docs](https://developers.fattureincloud.it/api-reference/#operation/createReceipt) |
| [Create Received Document](actions/create-received-document.md) | `POST /c/:company_id/received_documents` | [docs](https://developers.fattureincloud.it/api-reference/#operation/createReceivedDocument) |
| [Create Supplier](actions/create-supplier.md) | `POST /c/:company_id/entities/suppliers` | [docs](https://developers.fattureincloud.it/api-reference/#operation/createSupplier) |
| [Delete Client](actions/delete-client.md) | `DELETE /c/:company_id/entities/clients/:client_id` | [docs](https://developers.fattureincloud.it/api-reference/#operation/deleteClient) |
| [Delete Issued Document](actions/delete-issued-document.md) | `DELETE /c/:company_id/issued_documents/:document_id` | [docs](https://developers.fattureincloud.it/api-reference/#operation/deleteIssuedDocument) |
| [Delete Product](actions/delete-product.md) | `DELETE /c/:company_id/products/:product_id` | [docs](https://developers.fattureincloud.it/api-reference/#operation/deleteProduct) |
| [Delete Received Document](actions/delete-received-document.md) | `DELETE /c/:company_id/received_documents/:document_id` | [docs](https://developers.fattureincloud.it/api-reference/#operation/deleteReceivedDocument) |
| [Delete Supplier](actions/delete-supplier.md) | `DELETE /c/:company_id/entities/suppliers/:supplier_id` | [docs](https://developers.fattureincloud.it/api-reference/#operation/deleteSupplier) |
| [Get Client](actions/get-client.md) | `GET /c/:company_id/entities/clients/:client_id` | [docs](https://developers.fattureincloud.it/api-reference/#operation/getClient) |
| [Get Company Info](actions/get-company-info.md) | `GET /c/:company_id/company/info` | [docs](https://developers.fattureincloud.it/api-reference/#operation/getCompanyInfo) |
| [Get Issued Document](actions/get-issued-document.md) | `GET /c/:company_id/issued_documents/:document_id` | [docs](https://developers.fattureincloud.it/api-reference/#operation/getIssuedDocument) |
| [Get Product](actions/get-product.md) | `GET /c/:company_id/products/:product_id` | [docs](https://developers.fattureincloud.it/api-reference/#operation/getProduct) |
| [Get Receipt](actions/get-receipt.md) | `GET /c/:company_id/receipts/:document_id` | [docs](https://developers.fattureincloud.it/api-reference/#operation/getReceipt) |
| [Get Received Document](actions/get-received-document.md) | `GET /c/:company_id/received_documents/:document_id` | [docs](https://developers.fattureincloud.it/api-reference/#operation/getReceivedDocument) |
| [Get Supplier](actions/get-supplier.md) | `GET /c/:company_id/entities/suppliers/:supplier_id` | [docs](https://developers.fattureincloud.it/api-reference/#operation/getSupplier) |
| [List Clients](actions/list-clients.md) | `GET /c/:company_id/entities/clients` | [docs](https://developers.fattureincloud.it/api-reference/#operation/listClients) |
| [List Issued Documents](actions/list-issued-documents.md) | `GET /c/:company_id/issued_documents` | [docs](https://developers.fattureincloud.it/api-reference/#operation/listIssuedDocuments) |
| [List Products](actions/list-products.md) | `GET /c/:company_id/products` | [docs](https://developers.fattureincloud.it/api-reference/#operation/listProducts) |
| [List Receipts](actions/list-receipts.md) | `GET /c/:company_id/receipts` | [docs](https://developers.fattureincloud.it/api-reference/#operation/listReceipts) |
| [List Received Documents](actions/list-received-documents.md) | `GET /c/:company_id/received_documents` | [docs](https://developers.fattureincloud.it/api-reference/#operation/listReceivedDocuments) |
| [List Suppliers](actions/list-suppliers.md) | `GET /c/:company_id/entities/suppliers` | [docs](https://developers.fattureincloud.it/api-reference/#operation/listSuppliers) |
| [List User Companies](actions/list-user-companies.md) | `GET /user/companies` | [docs](https://developers.fattureincloud.it/api-reference/#operation/listUserCompanies) |
| [Modify Client](actions/modify-client.md) | `PUT /c/:company_id/entities/clients/:client_id` | [docs](https://developers.fattureincloud.it/api-reference/#operation/modifyClient) |
| [Modify Issued Document](actions/modify-issued-document.md) | `PUT /c/:company_id/issued_documents/:document_id` | [docs](https://developers.fattureincloud.it/api-reference/#operation/modifyIssuedDocument) |
| [Modify Product](actions/modify-product.md) | `PUT /c/:company_id/products/:product_id` | [docs](https://developers.fattureincloud.it/api-reference/#operation/modifyProduct) |
| [Modify Received Document](actions/modify-received-document.md) | `PUT /c/:company_id/received_documents/:document_id` | [docs](https://developers.fattureincloud.it/api-reference/#operation/modifyReceivedDocument) |
| [Modify Supplier](actions/modify-supplier.md) | `PUT /c/:company_id/entities/suppliers/:supplier_id` | [docs](https://developers.fattureincloud.it/api-reference/#operation/modifySupplier) |

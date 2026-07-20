# Sumtracker: Native API Reference

A consolidated summary of Sumtracker's API configuration and 38 documented operations, with links to official documentation.

- **Official docs:** https://developers.sumtracker.com/reference
- **OpenAPI specification:** https://developers.sumtracker.com/openapi/64ecdc34a5f19000285b3f7b
- **REST - Page Based base URL:** `https://inventory-api.sumtracker.com`
- **REST - Cursor base URL:** `https://inventory-api.sumtracker.com`

## Authentication

### API Key

Use a Sumtracker API key in the Authorization header as `Api-Key <api-key-value>`.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developers.sumtracker.com/reference/authentication-1)

## Pagination

- **REST - Page Based:** Use `limit` in the query string to set the page size (default 50; maximum 100). Use `offset` in the query string as the record offset; numbering starts at 0.
- **REST - Cursor:** Use `limit` in the query string to set the page size (default 50; maximum 100). Use `cursor` in the query string as the pagination cursor; numbering starts at 0.

## Retry behavior

- **REST - Page Based:** Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.
- **REST - Cursor:** Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (38 documented)

| Operation | API | Method & path | Vendor docs |
| --- | --- | --- | --- |
| [Create Goods Receipt Note](actions/create-grn.md) | REST - Page Based | `POST /api/version/2025-03/purchases/:document_type/:po_id/grns/` | [docs](https://developers.sumtracker.com/reference/grncreate) |
| [Create Goods Receipt Note Line](actions/create-grn-line.md) | REST - Page Based | `POST /api/version/2025-03/purchases/:document_type/:po_id/grns/:grn_id/lines/` | [docs](https://developers.sumtracker.com/reference/grnlinecreate) |
| [Create Purchase Order or Stock Transfer](actions/create-order.md) | REST - Page Based | `POST /api/version/2025-03/purchases/:document_type/` | [docs](https://developers.sumtracker.com/reference/purchaseordercreate) |
| [Create Purchase Order Line](actions/create-po-line.md) | REST - Page Based | `POST /api/version/2025-03/purchases/:document_type/:po_id/lines/` | [docs](https://developers.sumtracker.com/reference/polinecreate) |
| [Create Stock Adjustment Document](actions/create-stock-adjustment-document.md) | REST - Page Based | `POST /api/version/2025-03/stock/adjustment/documents/` | [docs](https://developers.sumtracker.com/reference/stockadjustmentdocumentcreate) |
| [Create Stock Adjustment Document Line](actions/create-stock-adjustment-document-line.md) | REST - Page Based | `POST /api/version/2025-03/stock/adjustment/documents/:document_id/lines/` | [docs](https://developers.sumtracker.com/reference/stockadjustmentdocumentlinecreate) |
| [Create Stock Adjustment Line](actions/create-stock-adjustment-line.md) | REST - Page Based | `POST /api/version/2025-03/stock/adjustment/` | [docs](https://developers.sumtracker.com/reference/stockadjustmentlinecreate) |
| [Delete Goods Receipt Note](actions/delete-grn.md) | REST - Page Based | `DELETE /api/version/2025-03/purchases/:document_type/:po_id/grns/:id/` | [docs](https://developers.sumtracker.com/reference/grndelete) |
| [Delete Goods Receipt Note Line](actions/delete-grn-line.md) | REST - Page Based | `DELETE /api/version/2025-03/purchases/:document_type/:po_id/grns/:grn_id/lines/:id/` | [docs](https://developers.sumtracker.com/reference/grnlinedelete) |
| [Delete Purchase Order Line](actions/delete-po-line.md) | REST - Page Based | `DELETE /api/version/2025-03/purchases/:document_type/:po_id/lines/:id/` | [docs](https://developers.sumtracker.com/reference/polinedelete) |
| [Delete Stock Adjustment Document](actions/delete-stock-adjustment-document.md) | REST - Page Based | `DELETE /api/version/2025-03/stock/adjustment/documents/:id/` | [docs](https://developers.sumtracker.com/reference/stockadjustmentdocumentdelete) |
| [Delete Stock Adjustment Document Line](actions/delete-stock-adjustment-document-line.md) | REST - Page Based | `DELETE /api/version/2025-03/stock/adjustment/documents/:document_id/lines/:id/` | [docs](https://developers.sumtracker.com/reference/stockadjustmentdocumentlinedelete) |
| [Get Goods Receipt Note](actions/get-grn.md) | REST - Page Based | `GET /api/version/2025-03/purchases/:document_type/:po_id/grns/:id/` | [docs](https://developers.sumtracker.com/reference/grnget) |
| [Get Purchase Order or Stock Transfer](actions/get-order.md) | REST - Page Based | `GET /api/version/2025-03/purchases/:document_type/:id/` | [docs](https://developers.sumtracker.com/reference/purchaseorderget) |
| [Get Stock Adjustment Document](actions/get-stock-adjustment-document.md) | REST - Page Based | `GET /api/version/2025-03/stock/adjustment/documents/:id/` | [docs](https://developers.sumtracker.com/reference/stockadjustmentdocumentget) |
| [List Bundle Components](actions/list-bundle-components.md) | REST - Page Based | `GET /api/version/2025-03/products/bundles/lines/` | [docs](https://developers.sumtracker.com/reference/bundlecomponentlist) |
| [List Bundle Stock Levels](actions/list-bundle-stock-levels.md) | REST - Cursor | `GET /api/version/2025-11/stock/levels/bundles/` | [docs](https://developers.sumtracker.com/reference/stocklevelbundlelist-1) |
| [List Goods Receipt Note Lines](actions/list-grn-lines.md) | REST - Page Based | `GET /api/version/2025-03/purchases/:document_type/:po_id/grns/:grn_id/lines/` | [docs](https://developers.sumtracker.com/reference/grnlinelist) |
| [List Goods Receipt Notes](actions/list-grns.md) | REST - Page Based | `GET /api/version/2025-03/purchases/:document_type/:po_id/grns/` | [docs](https://developers.sumtracker.com/reference/grnlist) |
| [List Purchase Orders or Stock Transfers](actions/list-orders.md) | REST - Page Based | `GET /api/version/2025-03/purchases/:document_type/` | [docs](https://developers.sumtracker.com/reference/purchaseorderlist) |
| [List Purchase Order Lines](actions/list-po-lines.md) | REST - Page Based | `GET /api/version/2025-03/purchases/:document_type/:po_id/lines/` | [docs](https://developers.sumtracker.com/reference/polinelist) |
| [List Products](actions/list-products.md) | REST - Page Based | `GET /api/version/2025-03/products/` | [docs](https://developers.sumtracker.com/reference/productlist) |
| [List Stock Adjustment Document Lines](actions/list-stock-adjustment-document-lines.md) | REST - Page Based | `GET /api/version/2025-03/stock/adjustment/documents/:document_id/lines/` | [docs](https://developers.sumtracker.com/reference/stockadjustmentdocumentlinelist) |
| [List Stock Adjustment Documents](actions/list-stock-adjustment-documents.md) | REST - Page Based | `GET /api/version/2025-03/stock/adjustment/documents/` | [docs](https://developers.sumtracker.com/reference/stockadjustmentdocumentlist) |
| [List Stock Levels](actions/list-stock-levels.md) | REST - Cursor | `GET /api/version/2025-11/stock/levels/` | [docs](https://developers.sumtracker.com/reference/stocklevellist-1) |
| [List Suppliers](actions/list-suppliers.md) | REST - Page Based | `GET /api/version/2025-03/purchases/contacts/` | [docs](https://developers.sumtracker.com/reference/supplierlist) |
| [List Taxes](actions/list-taxes.md) | REST - Page Based | `GET /api/version/2025-03/settings/taxes/` | [docs](https://developers.sumtracker.com/reference/taxlist) |
| [List Warehouses](actions/list-warehouses.md) | REST - Page Based | `GET /api/version/2025-03/settings/warehouses/` | [docs](https://developers.sumtracker.com/reference/warehouselist) |
| [Mark Stock Adjustment Complete](actions/mark-stock-adjustment-complete.md) | REST - Page Based | `PUT /api/version/2025-03/stock/adjustment/documents/perform_action/:id/mark-complete/` | [docs](https://developers.sumtracker.com/reference/performactionstockadjustment) |
| [Perform Goods Receipt Note Action](actions/perform-grn-action.md) | REST - Page Based | `PUT /api/version/2025-03/purchases/:document_type/:po_id/grns/perform_action/:id/:action/` | [docs](https://developers.sumtracker.com/reference/performactiongrn) |
| [Perform Purchase Order Action](actions/perform-order-action.md) | REST - Page Based | `PUT /api/version/2025-03/purchases/:document_type/perform_action/:id/:action/` | [docs](https://developers.sumtracker.com/reference/performactionpurchaseorder) |
| [Retrieve Supplier](actions/retrieve-supplier.md) | REST - Page Based | `GET /api/version/2025-03/purchases/contacts/:id/` | [docs](https://developers.sumtracker.com/reference/supplierretrieve) |
| [Update Goods Receipt Note](actions/update-grn.md) | REST - Page Based | `PUT /api/version/2025-03/purchases/:document_type/:po_id/grns/:id/` | [docs](https://developers.sumtracker.com/reference/grnupdate) |
| [Update Goods Receipt Note Line](actions/update-grn-line.md) | REST - Page Based | `PUT /api/version/2025-03/purchases/:document_type/:po_id/grns/:grn_id/lines/:id/` | [docs](https://developers.sumtracker.com/reference/grnlineupdate) |
| [Update Purchase Order or Stock Transfer](actions/update-order.md) | REST - Page Based | `PUT /api/version/2025-03/purchases/:document_type/:id/` | [docs](https://developers.sumtracker.com/reference/purchaseorderupdate) |
| [Update Purchase Order Line](actions/update-po-line.md) | REST - Page Based | `PUT /api/version/2025-03/purchases/:document_type/:po_id/lines/:id/` | [docs](https://developers.sumtracker.com/reference/polineupdate) |
| [Update Stock Adjustment Document](actions/update-stock-adjustment-document.md) | REST - Page Based | `PUT /api/version/2025-03/stock/adjustment/documents/:id/` | [docs](https://developers.sumtracker.com/reference/stockadjustmentdocumentupdate) |
| [Update Stock Adjustment Document Line](actions/update-stock-adjustment-document-line.md) | REST - Page Based | `PUT /api/version/2025-03/stock/adjustment/documents/:document_id/lines/:id/` | [docs](https://developers.sumtracker.com/reference/stockadjustmentdocumentlineupdate) |

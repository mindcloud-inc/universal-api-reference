# Acumatica: Native API Reference

A consolidated summary of Acumatica's API configuration and 27 documented operations, with links to official documentation.

- **Official docs:** https://help.acumatica.com/Help?ScreenId=ShowWiki&pageid=91dda8ed-5e92-48a5-a176-9a255506d0d6
- **API base URL:** `{uRL}`

## Authentication

### Custom

### Credentials

- **URL:** `uRL` · required · Acumatica instance URL. For example https://yourcompany.acumatica.com
- **Name:** `name` · optional
- **Password:** `password` · optional
- **Tenant:** `tenant` · optional
- **Branch:** `branch` · optional
- **Endpoint Name:** `endpointName` · optional
- **Endpoint Version:** `endpointVersion` · optional

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Pagination

Use `$top` in the query string to set the page size (default 25; accepted range 1–5000). Use `$skip` in the query string as the record offset.

## Endpoints (27 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Confirm Shipment](actions/confirm-shipment.md) | `PUT /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/Shipment/ConfirmShipment` | [docs](https://help.acumatica.com/(W(5))/Help?ScreenId=ShowWiki&pageid=56831ee7-14b0-45ef-8207-dace30beb2cb) |
| [Create Payment Link](actions/create-payment-link.md) | `POST /entity/:wse/:endpointVersion/SalesOrder/CreateLink` |  |
| [Create Project Task](actions/create-project-task.md) | `PUT /entity/:wse/:endpointVersion/ProjectTask` | [docs](https://github.com/Acumatica/AcumaticaRESTAPIClientForCSharp/blob/6.0/EndpointDefinitions/Default_24.200.001) |
| [Create/Update Sales Orders](actions/create-update-sales-orders.md) | `PUT /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/SalesOrder` |  |
| [Create/Update Shipment](actions/create-update-shipment.md) | `PUT /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/Shipment` | [docs](https://help.acumatica.com/(W(5))/Help?ScreenId=ShowWiki&pageid=56831ee7-14b0-45ef-8207-dace30beb2cb) |
| [Get Entity Schema](actions/entity-schema.md) | `GET /entity/Default/:endpointVersion/:entity/$adHocSchema` | [docs](https://help.acumatica.com/(W(5))/Help?ScreenId=ShowWiki&pageid=56831ee7-14b0-45ef-8207-dace30beb2cb) |
| [List Acumatica Endpoints](actions/get-acumatica-erp-endpoints.md) | `GET /entity/` | [docs](https://help.acumatica.com/(W(5))/Help?ScreenId=ShowWiki&pageid=1a9d6f7e-8546-426b-b1ff-d712fbcfbc7b) |
| [Get File](actions/get-file.md) | `GET /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/:entity` | [docs](https://help.acumatica.com/(W(5))/Help?ScreenId=ShowWiki&pageid=56831ee7-14b0-45ef-8207-dace30beb2cb) |
| [Get Inventory Quantity Available](actions/get-inventory-quantity-available.md) | `PUT /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/InventoryQuantityAvailable` | [docs](https://help.acumatica.com/(W(5))/Help?ScreenId=ShowWiki&pageid=56831ee7-14b0-45ef-8207-dace30beb2cb) |
| [Get Project Balance](actions/get-project-balance.md) | `GET /:projectId/:projectAction` | [docs](https://help.acumatica.com/(W(5))/Help?ScreenId=ShowWiki&pageid=56831ee7-14b0-45ef-8207-dace30beb2cb) |
| [Get Project by ID](actions/get-project-by-id.md) | `GET /:projectId` | [docs](https://help.acumatica.com/(W(5))/Help?ScreenId=ShowWiki&pageid=56831ee7-14b0-45ef-8207-dace30beb2cb) |
| [Get Purchase Order](actions/get-purchase-order.md) | `GET /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/PurchaseOrder` | [docs](https://help.acumatica.com/(W(5))/Help?ScreenId=ShowWiki&pageid=56831ee7-14b0-45ef-8207-dace30beb2cb) |
| [Get Purchase Orders List](actions/get-purchase-orders-list.md) | `GET /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/PurchaseOrders` | [docs](https://help.acumatica.com/(W(5))/Help?ScreenId=ShowWiki&pageid=56831ee7-14b0-45ef-8207-dace30beb2cb) |
| [Get Purchase Receipt](actions/get-purchase-receipt.md) | `GET /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/PurchaseReceipt` | [docs](https://help.acumatica.com/(W(5))/Help?ScreenId=ShowWiki&pageid=56831ee7-14b0-45ef-8207-dace30beb2cb) |
| [Get Sales Order](actions/get-sales-order.md) | `GET /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/SalesOrder/:orderType/:orderNbr` | [docs](https://beacon.acumatica.com/r/Integration-Development-Guide/REST-API-Examples/Basic-Requests/Retrieve-a-Record-by-Key-Fields) |
| [Inventory Adjustment](actions/inventory-adjustment.md) | `PUT /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/InventoryAdjustment` | [docs](https://help.acumatica.com/(W(5))/Help?ScreenId=ShowWiki&pageid=56831ee7-14b0-45ef-8207-dace30beb2cb) |
| [List Projects](actions/list-projects.md) | `GET /entity/:wse/:version/Project` | [docs](https://beacon.acumatica.com/r/Integration-Development-Guide/REST-API-Examples/Basic-Requests/Retrieve-Records-with-Attributes) |
| [List Sales Orders](actions/list-sales-orders.md) | `GET /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/SalesOrder` | [docs](https://beacon.acumatica.com/r/Integration-Development-Guide/REST-API-Examples/Basic-Requests/Retrieve-the-List-of-Records-in-Batches) |
| [Create Project](actions/new-action1.md) | `PUT /entity/:webServiceEndpoint/:endpointVersion/Project` | [docs](https://beacon.acumatica.com/r/Integration-Development-Guide/REST-API-Examples/Project/Create-a-Project-from-a-Project-Template?contentId=wJATI0KrOKqQ~ad2W48pHQ) |
| [Purchase Receipt](actions/purchase-receipt.md) | `PUT /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/PurchaseReceipt` | [docs](https://help.acumatica.com/(W(5))/Help?ScreenId=ShowWiki&pageid=56831ee7-14b0-45ef-8207-dace30beb2cb) |
| [Release Purchase Receipt](actions/release-purchase-receipt.md) | `POST /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/PurchaseReceipt/ReleasePurchaseReceipt` | [docs](https://help.acumatica.com/(W(5))/Help?ScreenId=ShowWiki&pageid=56831ee7-14b0-45ef-8207-dace30beb2cb) |
| [Reopen Shipment](actions/reopen-shipment.md) | `POST /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/SalesOrder/ReopenSalesOrder` | [docs](https://help.acumatica.com/(W(5))/Help?ScreenId=ShowWiki&pageid=56831ee7-14b0-45ef-8207-dace30beb2cb) |
| [Retrieve Stock Item](actions/retrieve-stock-item.md) | `GET /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/StockItem` | [docs](https://help.acumatica.com/(W(5))/Help?ScreenId=ShowWiki&pageid=56831ee7-14b0-45ef-8207-dace30beb2cb) |
| [Search By Entity](actions/search-by-entity.md) | `GET /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/:entity` | [docs](https://help.acumatica.com/(W(5))/Help?ScreenId=ShowWiki&pageid=56831ee7-14b0-45ef-8207-dace30beb2cb) |
| [Search By Generic Inquiry](actions/search-by-generic-inquiry.md) | `GET /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/:entity` | [docs](https://help.acumatica.com/(W(5))/Help?ScreenId=ShowWiki&pageid=56831ee7-14b0-45ef-8207-dace30beb2cb) |
| [Send Inventory Quantity(to Custom Field)](actions/send-inventory-quantityto-custom-field.md) | `PUT /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/ItemWarehouse` | [docs](https://help.acumatica.com/(W(5))/Help?ScreenId=ShowWiki&pageid=56831ee7-14b0-45ef-8207-dace30beb2cb) |
| [Update Sales Order](actions/update-sales-order.md) | `PUT /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/SalesOrder` | [docs](https://help.acumatica.com/(W(5))/Help?ScreenId=ShowWiki&pageid=56831ee7-14b0-45ef-8207-dace30beb2cb) |

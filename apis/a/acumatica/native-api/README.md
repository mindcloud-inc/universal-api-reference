# Acumatica: Native API Reference

A consolidated summary of Acumatica's API configuration and 55 documented operations, with links to official documentation.

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

## Endpoints (55 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Confirm Shipment](actions/confirm-shipment.md) | `PUT /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/Shipment/ConfirmShipment` | [docs](https://help.acumatica.com/(W(5))/Help?ScreenId=ShowWiki&pageid=56831ee7-14b0-45ef-8207-dace30beb2cb) |
| [Create or Update Contact](actions/create-or-update-contact.md) | `PUT /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/Contact` | [docs](https://help.acumatica.com/Wiki/ShowWiki.aspx?PageID=91dda8ed-5e92-48a5-a176-9a255506d0d6&wikiname=HelpRoot_Dev_Integration) |
| [Create or Update Customer](actions/create-or-update-customer.md) | `PUT /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/Customer` | [docs](https://help.acumatica.com/Wiki/ShowWiki.aspx?PageID=91dda8ed-5e92-48a5-a176-9a255506d0d6&wikiname=HelpRoot_Dev_Integration) |
| [Create or Update Opportunity](actions/create-or-update-opportunity.md) | `PUT /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/Opportunity` | [docs](https://help.acumatica.com/Wiki/ShowWiki.aspx?PageID=91dda8ed-5e92-48a5-a176-9a255506d0d6&wikiname=HelpRoot_Dev_Integration) |
| [Create or Update Sales Order](actions/create-or-update-sales-order.md) | `PUT /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/SalesOrder` | [docs](https://help.acumatica.com/Wiki/ShowWiki.aspx?PageID=91dda8ed-5e92-48a5-a176-9a255506d0d6&wikiname=HelpRoot_Dev_Integration) |
| [Create Payment](actions/create-payment.md) | `PUT /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/Payment` | [docs](https://help.acumatica.com/Wiki/ShowWiki.aspx?PageID=91dda8ed-5e92-48a5-a176-9a255506d0d6&wikiname=HelpRoot_Dev_Integration) |
| [Create Payment Link](actions/create-payment-link.md) | `POST /entity/:wse/:endpointVersion/SalesOrder/CreateLink` |  |
| [Create Project Task](actions/create-project-task.md) | `PUT /entity/:wse/:endpointVersion/ProjectTask` | [docs](https://github.com/Acumatica/AcumaticaRESTAPIClientForCSharp/blob/6.0/EndpointDefinitions/Default_24.200.001) |
| [Create/Update Shipment](actions/create-update-shipment.md) | `PUT /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/Shipment` | [docs](https://help.acumatica.com/(W(5))/Help?ScreenId=ShowWiki&pageid=56831ee7-14b0-45ef-8207-dace30beb2cb) |
| [Delete Sales Order](actions/delete-sales-order.md) | `DELETE /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/SalesOrder/:id` | [docs](https://help.acumatica.com/Wiki/ShowWiki.aspx?PageID=91dda8ed-5e92-48a5-a176-9a255506d0d6&wikiname=HelpRoot_Dev_Integration) |
| [Get Entity Schema](actions/entity-schema.md) | `GET /entity/Default/:endpointVersion/:entity/$adHocSchema` | [docs](https://help.acumatica.com/(W(5))/Help?ScreenId=ShowWiki&pageid=56831ee7-14b0-45ef-8207-dace30beb2cb) |
| [List Acumatica Endpoints](actions/get-acumatica-erp-endpoints.md) | `GET /entity/` | [docs](https://help.acumatica.com/(W(5))/Help?ScreenId=ShowWiki&pageid=1a9d6f7e-8546-426b-b1ff-d712fbcfbc7b) |
| [Get Bill](actions/get-bill.md) | `GET /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/Bill/:id` | [docs](https://beacon.acumatica.com/r/Integration-Development-Guide/REST-API-Examples/Basic-Requests/Retrieve-a-Record-by-ID) |
| [Get Contact](actions/get-contact.md) | `GET /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/Contact/:id` | [docs](https://beacon.acumatica.com/r/Integration-Development-Guide/REST-API-Examples/Basic-Requests/Retrieve-a-Record-by-ID) |
| [Get Customer](actions/get-customer.md) | `GET /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/Customer/:id` | [docs](https://beacon.acumatica.com/r/Integration-Development-Guide/REST-API-Examples/Basic-Requests/Retrieve-a-Record-by-ID) |
| [Get File](actions/get-file.md) | `GET /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/:entity` | [docs](https://help.acumatica.com/(W(5))/Help?ScreenId=ShowWiki&pageid=56831ee7-14b0-45ef-8207-dace30beb2cb) |
| [Get Inventory Quantity Available](actions/get-inventory-quantity-available.md) | `PUT /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/InventoryQuantityAvailable` | [docs](https://help.acumatica.com/(W(5))/Help?ScreenId=ShowWiki&pageid=56831ee7-14b0-45ef-8207-dace30beb2cb) |
| [Get Invoice](actions/get-invoice.md) | `GET /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/Invoice/:id` | [docs](https://beacon.acumatica.com/r/Integration-Development-Guide/REST-API-Examples/Basic-Requests/Retrieve-a-Record-by-ID) |
| [Get Opportunity](actions/get-opportunity.md) | `GET /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/Opportunity/:id` | [docs](https://beacon.acumatica.com/r/Integration-Development-Guide/REST-API-Examples/Basic-Requests/Retrieve-a-Record-by-ID) |
| [Get Project Balance](actions/get-project-balance.md) | `GET /:projectId/:projectAction` | [docs](https://help.acumatica.com/(W(5))/Help?ScreenId=ShowWiki&pageid=56831ee7-14b0-45ef-8207-dace30beb2cb) |
| [Get Project by ID](actions/get-project-by-id.md) | `GET /:projectId` | [docs](https://help.acumatica.com/(W(5))/Help?ScreenId=ShowWiki&pageid=56831ee7-14b0-45ef-8207-dace30beb2cb) |
| [Get Project Task](actions/get-project-task.md) | `GET /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/ProjectTask/:id` | [docs](https://beacon.acumatica.com/r/Integration-Development-Guide/REST-API-Examples/Basic-Requests/Retrieve-a-Record-by-ID) |
| [Get Purchase Order](actions/get-purchase-order.md) | `GET /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/PurchaseOrder/:id` | [docs](https://beacon.acumatica.com/r/Integration-Development-Guide/REST-API-Examples/Basic-Requests/Retrieve-a-Record-by-ID) |
| [List Purchase Orders](actions/get-purchase-orders-list.md) | `GET /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/PurchaseOrder` | [docs](https://beacon.acumatica.com/r/Integration-Development-Guide/REST-API-Examples/Basic-Requests/Retrieve-Records-by-Conditions) |
| [List Purchase Receipts](actions/get-purchase-receipt.md) | `GET /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/PurchaseReceipt` | [docs](https://beacon.acumatica.com/r/Integration-Development-Guide/REST-API-Examples/Basic-Requests/Retrieve-Records-by-Conditions) |
| [Get Sales Order](actions/get-sales-order.md) | `GET /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/SalesOrder/:orderType/:orderNbr` | [docs](https://beacon.acumatica.com/r/Integration-Development-Guide/REST-API-Examples/Basic-Requests/Retrieve-a-Record-by-Key-Fields) |
| [Get Shipment](actions/get-shipment.md) | `GET /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/Shipment/:id` | [docs](https://beacon.acumatica.com/r/Integration-Development-Guide/REST-API-Examples/Basic-Requests/Retrieve-a-Record-by-ID) |
| [Get Stock Item](actions/get-stock-item.md) | `GET /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/StockItem/:id` | [docs](https://beacon.acumatica.com/r/Integration-Development-Guide/REST-API-Examples/Basic-Requests/Retrieve-a-Record-by-ID) |
| [Get Vendor](actions/get-vendor.md) | `GET /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/Vendor/:id` | [docs](https://beacon.acumatica.com/r/Integration-Development-Guide/REST-API-Examples/Basic-Requests/Retrieve-a-Record-by-ID) |
| [Inventory Adjustment](actions/inventory-adjustment.md) | `PUT /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/InventoryAdjustment` | [docs](https://help.acumatica.com/(W(5))/Help?ScreenId=ShowWiki&pageid=56831ee7-14b0-45ef-8207-dace30beb2cb) |
| [List Bills](actions/list-bills.md) | `GET /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/Bill` | [docs](https://beacon.acumatica.com/r/Integration-Development-Guide/REST-API-Examples/Basic-Requests/Retrieve-Records-by-Conditions) |
| [List Contacts](actions/list-contacts.md) | `GET /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/Contact` | [docs](https://beacon.acumatica.com/r/Integration-Development-Guide/REST-API-Examples/Basic-Requests/Retrieve-Records-by-Conditions) |
| [List Customers](actions/list-customers.md) | `GET /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/Customer` | [docs](https://beacon.acumatica.com/r/Integration-Development-Guide/REST-API-Examples/Basic-Requests/Retrieve-Records-by-Conditions) |
| [List Invoices](actions/list-invoices.md) | `GET /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/Invoice` | [docs](https://beacon.acumatica.com/r/Integration-Development-Guide/REST-API-Examples/Basic-Requests/Retrieve-Records-by-Conditions) |
| [List Opportunities](actions/list-opportunities.md) | `GET /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/Opportunity` | [docs](https://beacon.acumatica.com/r/Integration-Development-Guide/REST-API-Examples/Basic-Requests/Retrieve-Records-by-Conditions) |
| [Get Payment](actions/list-payment-by-id.md) | `GET /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/Payment/:id` | [docs](https://beacon.acumatica.com/r/Integration-Development-Guide/REST-API-Examples/Basic-Requests/Retrieve-a-Record-by-ID) |
| [List Payments](actions/list-payments.md) | `GET /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/Payment` | [docs](https://beacon.acumatica.com/r/Integration-Development-Guide/REST-API-Examples/Basic-Requests/Retrieve-Records-by-Conditions) |
| [List Project Tasks](actions/list-project-tasks.md) | `GET /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/ProjectTask` | [docs](https://beacon.acumatica.com/r/Integration-Development-Guide/REST-API-Examples/Basic-Requests/Retrieve-Records-by-Conditions) |
| [List Projects](actions/list-projects.md) | `GET /entity/:wse/:version/Project` | [docs](https://beacon.acumatica.com/r/Integration-Development-Guide/REST-API-Examples/Basic-Requests/Retrieve-Records-with-Attributes) |
| [List Sales Orders](actions/list-sales-orders.md) | `GET /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/SalesOrder` | [docs](https://beacon.acumatica.com/r/Integration-Development-Guide/REST-API-Examples/Basic-Requests/Retrieve-the-List-of-Records-in-Batches) |
| [List Shipments](actions/list-shipments.md) | `GET /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/Shipment` | [docs](https://beacon.acumatica.com/r/Integration-Development-Guide/REST-API-Examples/Basic-Requests/Retrieve-Records-by-Conditions) |
| [List Vendors](actions/list-vendors.md) | `GET /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/Vendor` | [docs](https://beacon.acumatica.com/r/Integration-Development-Guide/REST-API-Examples/Basic-Requests/Retrieve-Records-by-Conditions) |
| [Create Project](actions/new-action1.md) | `PUT /entity/:webServiceEndpoint/:endpointVersion/Project` | [docs](https://beacon.acumatica.com/r/Integration-Development-Guide/REST-API-Examples/Project/Create-a-Project-from-a-Project-Template?contentId=wJATI0KrOKqQ~ad2W48pHQ) |
| [Purchase Receipt](actions/purchase-receipt.md) | `PUT /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/PurchaseReceipt` | [docs](https://help.acumatica.com/(W(5))/Help?ScreenId=ShowWiki&pageid=56831ee7-14b0-45ef-8207-dace30beb2cb) |
| [Release Payment](actions/release-payment.md) | `POST /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/Payment/ReleasePayment` | [docs](https://help.acumatica.com/Wiki/ShowWiki.aspx?PageID=91dda8ed-5e92-48a5-a176-9a255506d0d6&wikiname=HelpRoot_Dev_Integration) |
| [Release Purchase Receipt](actions/release-purchase-receipt.md) | `POST /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/PurchaseReceipt/ReleasePurchaseReceipt` | [docs](https://help.acumatica.com/(W(5))/Help?ScreenId=ShowWiki&pageid=56831ee7-14b0-45ef-8207-dace30beb2cb) |
| [Reopen Shipment](actions/reopen-shipment.md) | `POST /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/SalesOrder/ReopenSalesOrder` | [docs](https://help.acumatica.com/(W(5))/Help?ScreenId=ShowWiki&pageid=56831ee7-14b0-45ef-8207-dace30beb2cb) |
| [List Stock Items](actions/retrieve-stock-item.md) | `GET /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/StockItem` | [docs](https://beacon.acumatica.com/r/Integration-Development-Guide/REST-API-Examples/Basic-Requests/Retrieve-Records-by-Conditions) |
| [Reverse Bill](actions/reverse-bill.md) | `POST /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/Bill/ReverseBill` | [docs](https://help.acumatica.com/Wiki/ShowWiki.aspx?PageID=91dda8ed-5e92-48a5-a176-9a255506d0d6&wikiname=HelpRoot_Dev_Integration) |
| [Search By Entity](actions/search-by-entity.md) | `GET /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/:entity` | [docs](https://help.acumatica.com/(W(5))/Help?ScreenId=ShowWiki&pageid=56831ee7-14b0-45ef-8207-dace30beb2cb) |
| [Search By Generic Inquiry](actions/search-by-generic-inquiry.md) | `GET /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/:entity` | [docs](https://help.acumatica.com/(W(5))/Help?ScreenId=ShowWiki&pageid=56831ee7-14b0-45ef-8207-dace30beb2cb) |
| [Send Inventory Quantity(to Custom Field)](actions/send-inventory-quantityto-custom-field.md) | `PUT /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/ItemWarehouse` | [docs](https://help.acumatica.com/(W(5))/Help?ScreenId=ShowWiki&pageid=56831ee7-14b0-45ef-8207-dace30beb2cb) |
| [Update Sales Order](actions/update-sales-order.md) | `PUT /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/SalesOrder` | [docs](https://help.acumatica.com/(W(5))/Help?ScreenId=ShowWiki&pageid=56831ee7-14b0-45ef-8207-dace30beb2cb) |
| [Update Stock Item Standard Cost](actions/update-stock-item-standard-cost.md) | `POST /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/StockItem/UpdateStandardCostStockItem` | [docs](https://help.acumatica.com/Wiki/ShowWiki.aspx?PageID=91dda8ed-5e92-48a5-a176-9a255506d0d6&wikiname=HelpRoot_Dev_Integration) |
| [Void Payment](actions/void-payment.md) | `POST /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/Payment/VoidPayment` | [docs](https://help.acumatica.com/Wiki/ShowWiki.aspx?PageID=91dda8ed-5e92-48a5-a176-9a255506d0d6&wikiname=HelpRoot_Dev_Integration) |

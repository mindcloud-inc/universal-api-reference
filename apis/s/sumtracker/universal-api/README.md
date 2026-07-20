# <img src="https://images.mindcloud.co/apps/icons/sumtracker-1772520892719_1778000910065.png" alt="Sumtracker logo" width="28" height="28"> Sumtracker: Universal API

Sumtracker is an inventory management platform for ecommerce merchants. This wrapper exposes products, bundle components, stock levels, suppliers, warehouses, purchase orders, stock adjustments, and goods receipt notes through Sumtracker's public API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/sumtracker/latest
- **Category:** Commerce / Supply Chain
- **Actions:** 38
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://sumtracker.com
- **Vendor API docs:** https://developers.sumtracker.com/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Warehouses](actions/list-warehouses.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sumtracker/latest/actions/list-warehouses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (38)

### Goods Receipt Notes

| Action | Method | Description |
| --- | --- | --- |
| [Create Goods Receipt Note](actions/create-grn.md) | POST | Creates a goods receipt note in Sumtracker. |
| [Create Goods Receipt Note Line](actions/create-grn-line.md) | POST | Creates a goods receipt note line in Sumtracker. |
| [Delete Goods Receipt Note](actions/delete-grn.md) | DELETE | Deletes a goods receipt note from Sumtracker. |
| [Delete Goods Receipt Note Line](actions/delete-grn-line.md) | DELETE | Deletes a goods receipt note line from Sumtracker. |
| [Get Goods Receipt Note](actions/get-grn.md) | GET | Retrieves a goods receipt note from Sumtracker. |
| [List Goods Receipt Note Lines](actions/list-grn-lines.md) | GET | Retrieves goods receipt note lines from Sumtracker. |
| [List Goods Receipt Notes](actions/list-grns.md) | GET | Retrieves goods receipt notes from Sumtracker. |
| [Perform Goods Receipt Note Action](actions/perform-grn-action.md) | PUT | Performs an action on a goods receipt note in Sumtracker. |
| [Update Goods Receipt Note](actions/update-grn.md) | PUT | Updates a goods receipt note in Sumtracker. |
| [Update Goods Receipt Note Line](actions/update-grn-line.md) | PUT | Updates a goods receipt note line in Sumtracker. |

### Products

| Action | Method | Description |
| --- | --- | --- |
| [List Bundle Components](actions/list-bundle-components.md) | GET | Retrieves bundle components from Sumtracker. |
| [List Products](actions/list-products.md) | GET | Retrieves products from Sumtracker. |

### Purchase Orders

| Action | Method | Description |
| --- | --- | --- |
| [Create Purchase Order or Stock Transfer](actions/create-order.md) | POST | Creates a purchase order or stock transfer in Sumtracker. |
| [Create Purchase Order Line](actions/create-po-line.md) | POST | Creates a purchase order line in Sumtracker. |
| [Delete Purchase Order Line](actions/delete-po-line.md) | DELETE | Deletes a purchase order line from Sumtracker. |
| [Get Purchase Order or Stock Transfer](actions/get-order.md) | GET | Retrieves a purchase order or stock transfer from Sumtracker. |
| [List Purchase Orders or Stock Transfers](actions/list-orders.md) | GET | Retrieves purchase orders or stock transfers from Sumtracker. |
| [List Purchase Order Lines](actions/list-po-lines.md) | GET | Retrieves purchase order lines from Sumtracker. |
| [Perform Purchase Order Action](actions/perform-order-action.md) | PUT | Performs an action on a purchase order in Sumtracker. |
| [Update Purchase Order or Stock Transfer](actions/update-order.md) | PUT | Updates a purchase order or stock transfer in Sumtracker. |
| [Update Purchase Order Line](actions/update-po-line.md) | PUT | Updates a purchase order line in Sumtracker. |

### Settings

| Action | Method | Description |
| --- | --- | --- |
| [List Taxes](actions/list-taxes.md) | GET | Retrieves tax rates from Sumtracker. |
| [List Warehouses](actions/list-warehouses.md) | GET | Retrieves warehouses from Sumtracker. |

### Stock Adjustments

| Action | Method | Description |
| --- | --- | --- |
| [Create Stock Adjustment Document](actions/create-stock-adjustment-document.md) | POST | Creates a stock adjustment document in Sumtracker. |
| [Create Stock Adjustment Document Line](actions/create-stock-adjustment-document-line.md) | POST | Creates a stock adjustment document line in Sumtracker. |
| [Create Stock Adjustment Line](actions/create-stock-adjustment-line.md) | POST | Creates a stock adjustment line in Sumtracker. |
| [Delete Stock Adjustment Document](actions/delete-stock-adjustment-document.md) | DELETE | Deletes a stock adjustment document from Sumtracker. |
| [Delete Stock Adjustment Document Line](actions/delete-stock-adjustment-document-line.md) | DELETE | Deletes a stock adjustment document line from Sumtracker. |
| [Get Stock Adjustment Document](actions/get-stock-adjustment-document.md) | GET | Retrieves a stock adjustment document from Sumtracker. |
| [List Stock Adjustment Document Lines](actions/list-stock-adjustment-document-lines.md) | GET | Retrieves stock adjustment document lines from Sumtracker. |
| [List Stock Adjustment Documents](actions/list-stock-adjustment-documents.md) | GET | Retrieves stock adjustment documents from Sumtracker. |
| [Mark Stock Adjustment Complete](actions/mark-stock-adjustment-complete.md) | PUT | Marks a stock adjustment document complete in Sumtracker. |
| [Update Stock Adjustment Document](actions/update-stock-adjustment-document.md) | PUT | Updates a stock adjustment document in Sumtracker. |
| [Update Stock Adjustment Document Line](actions/update-stock-adjustment-document-line.md) | PUT | Updates a stock adjustment document line in Sumtracker. |

### Stock Levels

| Action | Method | Description |
| --- | --- | --- |
| [List Bundle Stock Levels](actions/list-bundle-stock-levels.md) | GET | Retrieves bundle stock levels from Sumtracker. |
| [List Stock Levels](actions/list-stock-levels.md) | GET | Retrieves stock levels from Sumtracker. |

### Suppliers

| Action | Method | Description |
| --- | --- | --- |
| [List Suppliers](actions/list-suppliers.md) | GET | Retrieves suppliers from Sumtracker. |
| [Retrieve Supplier](actions/retrieve-supplier.md) | GET | Retrieves a supplier from Sumtracker. |


# <img src="https://images.mindcloud.co/apps/icons/disco-1759423730800_1776796876668.png" alt="Rithum DSCO logo" width="28" height="28"> Rithum DSCO: Universal API

Rithum DSCO provides commerce operations APIs for suppliers and retailers to manage orders, inventory, catalog data, shipments, invoices, returns, warehouses, trading partners, conversations, shipping labels, and related marketplace workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/rithumDSCOV2/latest
- **Category:** Commerce
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.rithum.com/
- **Vendor API docs:** https://api.dsco.io/doc/v3/reference/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Test Connection](actions/test-connection.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rithumDSCOV2/latest/actions/test-connection?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Assortment

| Action | Method | Description |
| --- | --- | --- |
| [Create Assortment](actions/create-assortment.md) | POST | Creates an assortment in Rithum DSCO. |
| [Delete Assortment](actions/delete-assortment.md) | DELETE | Deletes an assortment from Rithum DSCO. |
| [Get Assortment](actions/get-assortment.md) | GET | Retrieves an assortment from Rithum DSCO. |
| [List Assortments](actions/get-assortments.md) | GET | Lists assortments in Rithum DSCO. |
| [Update Assortment](actions/update-assortment.md) | PUT | Updates an assortment in Rithum DSCO. |

### Catalog Change Log

| Action | Method | Description |
| --- | --- | --- |
| [Get Catalog Change Log](actions/get-catalog-change-log.md) | GET | Retrieves the catalog change log from Rithum DSCO. |

### Catalog Item

| Action | Method | Description |
| --- | --- | --- |
| [Get Catalog Object](actions/get-catalog-by-id.md) | GET | Retrieves a catalog item from Rithum DSCO. |
| [Update Catalog Small Batch](actions/update-catalog-small-batch.md) | PUT | Updates catalog items in a small batch in Rithum DSCO. |

### Connection Test

| Action | Method | Description |
| --- | --- | --- |
| [Test Connection](actions/test-connection.md) | GET | Retrieves a hello-world response from Rithum DSCO. |

### Inventory

| Action | Method | Description |
| --- | --- | --- |
| [Get Inventory Object](actions/get-inventory-by-id.md) | GET | Retrieves an inventory record from Rithum DSCO. |
| [Update Single Inventory](actions/single-item.md) | PUT | Updates a single inventory record in Rithum DSCO. |

### Invoice

| Action | Method | Description |
| --- | --- | --- |
| [Create Invoice Small Batch](actions/create-invoice-small-batch.md) | POST |  |
| [Get Invoice](actions/get-invoice-by-id.md) | GET | Retrieves an invoice from Rithum DSCO. |
| [Create Invoice](actions/single-invoice.md) | POST | Creates an invoice in Rithum DSCO. |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [Acknowledge Orders](actions/acknowledge-orders.md) | PUT | Acknowledges orders in Rithum DSCO. |
| [Create Order](actions/create-order.md) | POST | Creates an order in Rithum DSCO. |
| [Get Order](actions/get-order-by-id.md) | GET | Retrieves an order from Rithum DSCO. |
| [List Orders](actions/list-orders.md) | GET | Lists orders in Rithum DSCO. |

### Order Change Log

| Action | Method | Description |
| --- | --- | --- |
| [Get Order Change Log](actions/get-order-change-log.md) | GET | Retrieves the order change log from Rithum DSCO. |

### Order Item

| Action | Method | Description |
| --- | --- | --- |
| [Acknowledge Order Items](actions/acknowledge-order-items.md) | PUT | Acknowledges order items in Rithum DSCO. |
| [Cancel Order Item](actions/cancel-order-item.md) | PUT | Cancels an order item in Rithum DSCO. |

### Shipment

| Action | Method | Description |
| --- | --- | --- |
| [Create Shipment Small Batch](actions/create-shipment-small-batch.md) | POST |  |
| [Create Shipment](actions/single-shipment.md) | POST | Creates a shipment in Rithum DSCO. |

### Warehouse

| Action | Method | Description |
| --- | --- | --- |
| [Get Warehouses](actions/get-warehouses.md) | GET | Lists warehouses in Rithum DSCO. |


# <img src="https://images.mindcloud.co/apps/icons/images-4_1774373670679.png" alt="TrackMage logo" width="28" height="28"> TrackMage: Universal API

TrackMage helps teams manage workspaces, orders, shipments, shipment items, products, product variants, and workflows through a REST API delivered as JSON and LD+JSON over HTTPS.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/trackMage/latest
- **Category:** Commerce
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://trackmage.com
- **Vendor API docs:** https://docs.trackmage.com/docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Workspaces](actions/list-workspaces.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trackMage/latest/actions/list-workspaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Event

| Action | Method | Description |
| --- | --- | --- |
| [List Shipment Checkpoints](actions/list-shipment-checkpoints.md) | GET | Retrieves shipment checkpoints for a shipment in TrackMage. |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [Create Order](actions/create-order.md) | POST | Creates a new order in TrackMage. |
| [Delete Order](actions/delete-order.md) | DELETE | Deletes an existing order from TrackMage. |
| [Get Order](actions/get-order.md) | GET | Retrieves an order from your TrackMage account. |
| [List Orders](actions/list-orders.md) | GET | Retrieves orders from your TrackMage account. |
| [Lookup Order](actions/lookup-order.md) | GET | Finds an order in TrackMage by search criteria. |
| [Update Order](actions/update-order.md) | PUT | Updates an existing order in TrackMage. |

### Order Line

| Action | Method | Description |
| --- | --- | --- |
| [List Order Items For Order](actions/list-order-items-for-order.md) | GET | Retrieves order items for an order in TrackMage. |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [Create Product](actions/create-product.md) | POST | Creates a new product in TrackMage. |
| [Delete Product](actions/delete-product.md) | DELETE | Deletes an existing product from TrackMage. |
| [Get Product](actions/get-product.md) | GET | Retrieves a product from your TrackMage account. |
| [List Products](actions/list-products.md) | GET | Retrieves products from your TrackMage account. |
| [Update Product](actions/update-product.md) | PUT | Updates an existing product in TrackMage. |

### Product Variant

| Action | Method | Description |
| --- | --- | --- |
| [Create Product Variant](actions/create-product-variant.md) | POST | Creates a new product variant in TrackMage. |
| [Delete Product Variant](actions/delete-product-variant.md) | DELETE | Deletes an existing product variant from TrackMage. |
| [Get Product Variant](actions/get-product-variant.md) | GET | Retrieves a product variant from TrackMage. |
| [List Product Variants](actions/list-product-variants.md) | GET | Retrieves product variants from your TrackMage account. |
| [Update Product Variant](actions/update-product-variant.md) | PUT | Updates an existing product variant in TrackMage. |

### Shipment

| Action | Method | Description |
| --- | --- | --- |
| [Create Shipment](actions/create-shipment.md) | POST | Creates a new shipment in TrackMage. |
| [Delete Shipment](actions/delete-shipment.md) | DELETE | Deletes an existing shipment from TrackMage. |
| [Get Shipment](actions/get-shipment.md) | GET | Retrieves a shipment from your TrackMage account. |
| [List Shipments](actions/list-shipments.md) | GET | Retrieves shipments from your TrackMage account. |
| [Lookup Shipment](actions/lookup-shipment.md) | GET | Finds a shipment in TrackMage by search criteria. |
| [Merge Shipments](actions/merge-shipments.md) | PUT | Merges shipments into one shipment in TrackMage. |
| [Update Shipment](actions/update-shipment.md) | PUT | Updates an existing shipment in TrackMage. |

### Shipment Item

| Action | Method | Description |
| --- | --- | --- |
| [Create Shipment Item](actions/create-shipment-item.md) | POST | Creates a new shipment item in TrackMage. |
| [Delete Shipment Item](actions/delete-shipment-item.md) | DELETE | Deletes an existing shipment item from TrackMage. |
| [Get Shipment Item](actions/get-shipment-item.md) | GET | Retrieves a shipment item from TrackMage. |
| [List Shipment Items](actions/list-shipment-items.md) | GET | Retrieves shipment items from your TrackMage account. |
| [List Shipment Items For Shipment](actions/list-shipment-items-for-shipment.md) | GET | Retrieves shipment items for a shipment in TrackMage. |
| [Update Shipment Item](actions/update-shipment-item.md) | PUT | Updates an existing shipment item in TrackMage. |

### Workflow

| Action | Method | Description |
| --- | --- | --- |
| [Create Workflow](actions/create-workflow.md) | POST | Creates a new workflow in TrackMage. |
| [Execute Workflow](actions/execute-workflow.md) | PUT | Executes a workflow in your TrackMage account. |
| [Get Workflow](actions/get-workflow.md) | GET | Retrieves a workflow from your TrackMage account. |
| [List Workflows](actions/list-workflows.md) | GET | Retrieves workflows from your TrackMage account. |

### Workspace

| Action | Method | Description |
| --- | --- | --- |
| [Create Workspace](actions/create-workspace.md) | POST | Creates a new workspace in TrackMage. |
| [Delete Workspace](actions/delete-workspace.md) | DELETE | Deletes an existing workspace from TrackMage. |
| [Get Workspace](actions/get-workspace.md) | GET | Retrieves a workspace from your TrackMage account. |
| [List Workspaces](actions/list-workspaces.md) | GET | Retrieves workspaces from your TrackMage account. |
| [Update Workspace](actions/update-workspace.md) | PUT | Updates an existing workspace in TrackMage. |


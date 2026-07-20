# <img src="https://images.mindcloud.co/apps/icons/katana_1773932294576.png" alt="Katana logo" width="28" height="28"> Katana: Universal API

Katana is a cloud manufacturing and inventory management platform for products, variants, materials, inventory, purchasing, sales, and production operations.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/katana/latest
- **Category:** Commerce / Supply Chain
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://katanamrp.com/
- **Vendor API docs:** https://developer.katanamrp.com/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Retrieve Current Factory](actions/retrieve-current-factory.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/katana/latest/actions/retrieve-current-factory?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | POST | Creates a new customer in Katana. |
| [List Customers](actions/list-customers.md) | GET | Lists customers in your Katana account. |
| [Update Customer](actions/update-customer.md) | PUT | Updates an existing customer in Katana. |

### Factory

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Current Factory](actions/retrieve-current-factory.md) | GET | Retrieves the current factory from Katana. |

### Inventory

| Action | Method | Description |
| --- | --- | --- |
| [List Current Inventory](actions/list-current-inventory.md) | GET | Lists current inventory records in Katana. |
| [List Variants with Negative Stock](actions/list-variants-with-negative-stock.md) | GET | Lists variants with negative stock in Katana. |

### Inventory Movement

| Action | Method | Description |
| --- | --- | --- |
| [List Inventory Movements](actions/list-inventory-movements.md) | GET | Lists inventory movements in your Katana account. |

### Inventory Reorder Point

| Action | Method | Description |
| --- | --- | --- |
| [Update Reorder Point](actions/update-reorder-point.md) | PUT | Updates an inventory reorder point in Katana. |

### Inventory Safety Stock Level

| Action | Method | Description |
| --- | --- | --- |
| [Update Safety Stock Level](actions/update-safety-stock-level.md) | PUT | Updates an inventory safety stock level in Katana. |

### Location

| Action | Method | Description |
| --- | --- | --- |
| [List Locations](actions/list-locations.md) | GET | Lists locations in your Katana account. |

### Manufacturing Order

| Action | Method | Description |
| --- | --- | --- |
| [Create Manufacturing Order](actions/create-manufacturing-order.md) | POST | Creates a new manufacturing order in Katana. |
| [List Manufacturing Orders](actions/list-manufacturing-orders.md) | GET | Lists manufacturing orders in your Katana account. |
| [Retrieve Manufacturing Order](actions/retrieve-manufacturing-order.md) | GET | Retrieves a manufacturing order by ID from Katana. |
| [Update Manufacturing Order](actions/update-manufacturing-order.md) | PUT | Updates an existing manufacturing order in Katana. |

### Material

| Action | Method | Description |
| --- | --- | --- |
| [Create Material](actions/create-material.md) | POST | Creates a new material in Katana. |
| [List Materials](actions/list-materials.md) | GET | Lists materials in your Katana account. |
| [Retrieve Material](actions/retrieve-material.md) | GET | Retrieves a material by ID from Katana. |
| [Update Material](actions/update-material.md) | PUT | Updates an existing material in Katana. |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [Create Product](actions/create-product.md) | POST | Creates a new product in Katana. |
| [List Products](actions/list-products.md) | GET | Lists products in your Katana account. |
| [Retrieve Product](actions/retrieve-product.md) | GET | Retrieves a product by ID from Katana. |
| [Update Product](actions/update-product.md) | PUT | Updates an existing product in Katana. |

### Purchase Order

| Action | Method | Description |
| --- | --- | --- |
| [Create Purchase Order](actions/create-purchase-order.md) | POST | Creates a new purchase order in Katana. |
| [List Purchase Orders](actions/list-purchase-orders.md) | GET | Lists purchase orders in your Katana account. |
| [Receive Purchase Order](actions/receive-purchase-order.md) | PUT | Marks a purchase order as received in Katana. |
| [Retrieve Purchase Order](actions/retrieve-purchase-order.md) | GET | Retrieves a purchase order by ID from Katana. |
| [Update Purchase Order](actions/update-purchase-order.md) | PUT | Updates an existing purchase order in Katana. |

### Sales Order

| Action | Method | Description |
| --- | --- | --- |
| [Create Sales Order](actions/create-sales-order.md) | POST | Creates a new sales order in Katana. |
| [List Sales Orders](actions/list-sales-orders.md) | GET | Lists sales orders in your Katana account. |
| [Retrieve Sales Order](actions/retrieve-sales-order.md) | GET | Retrieves a sales order by ID from Katana. |
| [Update Sales Order](actions/update-sales-order.md) | PUT | Updates an existing sales order in Katana. |

### Sales Order Fulfillment

| Action | Method | Description |
| --- | --- | --- |
| [Create Sales Order Fulfillment](actions/create-sales-order-fulfillment.md) | POST | Creates a sales order fulfillment in Katana. |
| [List Sales Order Fulfillments](actions/list-sales-order-fulfillments.md) | GET | Lists sales order fulfillments in Katana. |

### Supplier

| Action | Method | Description |
| --- | --- | --- |
| [Create Supplier](actions/create-supplier.md) | POST | Creates a new supplier in Katana. |
| [List Suppliers](actions/list-suppliers.md) | GET | Lists suppliers in your Katana account. |
| [Update Supplier](actions/update-supplier.md) | PUT | Updates an existing supplier in Katana. |

### Variant

| Action | Method | Description |
| --- | --- | --- |
| [Create Variant](actions/create-variant.md) | POST | Creates a new variant in Katana. |
| [List Variants](actions/list-variants.md) | GET | Lists variants in your Katana account. |
| [Retrieve Variant](actions/retrieve-variant.md) | GET | Retrieves a variant by ID from Katana. |
| [Update Variant](actions/update-variant.md) | PUT | Updates an existing variant in Katana. |


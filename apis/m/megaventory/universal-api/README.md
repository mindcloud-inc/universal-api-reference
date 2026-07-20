# <img src="https://images.mindcloud.co/apps/icons/megaventory_1774904992210.png" alt="Megaventory logo" width="28" height="28"> Megaventory: Universal API

Manage inventory, orders, products, suppliers, and manufacturing workflows

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/megaventory/latest
- **Category:** Commerce / ERP
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://megaventory.com
- **Vendor API docs:** https://api.megaventory.com/v2017a/metadata

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Products](actions/list-products.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/megaventory/latest/actions/list-products?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Contact Person

| Action | Method | Description |
| --- | --- | --- |
| [List Contact Persons](actions/list-contact-persons.md) | GET | Retrieves contact person records from Megaventory. |
| [Update Contact Person](actions/update-contact-person.md) | PUT | Updates a contact person in Megaventory using a record action. |

### Inventory Level

| Action | Method | Description |
| --- | --- | --- |
| [List Inventory Levels](actions/list-inventory-levels.md) | GET | Retrieves inventory level records from Megaventory. |
| [Update Inventory Levels](actions/update-inventory-levels.md) | PUT | Updates inventory levels in Megaventory. |

### Inventory Location

| Action | Method | Description |
| --- | --- | --- |
| [List Inventory Locations](actions/list-inventory-locations.md) | GET | Retrieves inventory location records from Megaventory. |
| [Update Inventory Location](actions/update-inventory-location.md) | PUT | Updates an inventory location in Megaventory using a record action. |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [List Products](actions/list-products.md) | GET | Retrieves existing product records from Megaventory. |
| [Update Product](actions/update-product.md) | PUT | Updates a product in Megaventory using a record action. |

### Product Category

| Action | Method | Description |
| --- | --- | --- |
| [List Product Categories](actions/list-product-categories.md) | GET | Retrieves product category records from Megaventory. |
| [Update Product Category](actions/update-product-category.md) | PUT | Updates a product category in Megaventory using a record action. |

### Product Client

| Action | Method | Description |
| --- | --- | --- |
| [List Product Clients](actions/list-product-clients.md) | GET | Retrieves product client links from Megaventory. |
| [Update Product Client](actions/update-product-client.md) | PUT | Updates a product client link in Megaventory using a record action. |

### Product Price

| Action | Method | Description |
| --- | --- | --- |
| [Get Product Pricing](actions/get-product-pricing.md) | GET | Retrieves pricing for a product from Megaventory. |

### Product Supplier

| Action | Method | Description |
| --- | --- | --- |
| [List Product Suppliers](actions/list-product-suppliers.md) | GET | Retrieves product supplier links from Megaventory. |
| [Update Product Supplier](actions/update-product-supplier.md) | PUT | Updates a product supplier link in Megaventory using a record action. |

### Purchase Order

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Update Purchase Orders](actions/bulk-update-purchase-orders.md) | PUT | Updates purchase orders in Megaventory in bulk. |
| [Cancel Purchase Order](actions/cancel-purchase-order.md) | PUT | Cancels a purchase order in Megaventory. |
| [List Purchase Orders](actions/list-purchase-orders.md) | GET | Retrieves purchase order records from Megaventory. |
| [Update Purchase Order](actions/update-purchase-order.md) | PUT | Updates a purchase order in Megaventory using a record action. |

### Sales Order

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Update Sales Orders](actions/bulk-update-sales-orders.md) | PUT | Updates sales orders in Megaventory in bulk. |
| [Cancel Sales Order](actions/cancel-sales-order.md) | PUT | Cancels a sales order in Megaventory. |
| [List Sales Orders](actions/list-sales-orders.md) | GET | Retrieves sales order records from Megaventory. |
| [Update Sales Order](actions/update-sales-order.md) | PUT | Updates a sales order in Megaventory using a record action. |

### Sales Quote

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Update Sales Quotes](actions/bulk-update-sales-quotes.md) | PUT | Updates sales quotes in Megaventory in bulk. |
| [List Sales Quotes](actions/list-sales-quotes.md) | GET | Retrieves sales quote records from Megaventory. |
| [Update Sales Quote](actions/update-sales-quote.md) | PUT | Updates a sales quote in Megaventory using a record action. |

### Supplier Or Client

| Action | Method | Description |
| --- | --- | --- |
| [List Suppliers and Clients](actions/list-suppliers-and-clients.md) | GET | Retrieves supplier and client records from Megaventory. |
| [Update Supplier or Client](actions/update-supplier-or-client.md) | PUT | Updates a supplier or client in Megaventory using a record action. |

### Supplier Stock

| Action | Method | Description |
| --- | --- | --- |
| [List Supplier Stock](actions/list-supplier-stock.md) | GET | Retrieves supplier stock records from Megaventory. |
| [Update Supplier Stock](actions/update-supplier-stock.md) | PUT | Updates supplier stock in Megaventory using a record action. |


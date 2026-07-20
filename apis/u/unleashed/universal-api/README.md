# <img src="https://images.mindcloud.co/apps/icons/unleashed_1775770826916.png" alt="Unleashed logo" width="28" height="28"> Unleashed: Universal API

Manage inventory, products, customers, orders, and warehouses

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/unleashed/latest
- **Category:** Commerce / Supply Chain
- **Actions:** 27
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.unleashedsoftware.com
- **Vendor API docs:** https://apidocs.unleashedsoftware.com

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Products](actions/list-products.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/unleashed/latest/actions/list-products?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (27)

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | POST | Creates a new customer in Unleashed. |
| [Get Customer](actions/get-customer.md) | GET | Retrieves a customer from your Unleashed customer directory. |
| [List Customers](actions/list-customers.md) | GET | Retrieves customers from your Unleashed customer directory. |
| [Update Customer](actions/update-customer.md) | PUT | Updates an existing customer in Unleashed. |

### Customer Contact

| Action | Method | Description |
| --- | --- | --- |
| [List Customer Contacts](actions/list-customer-contacts.md) | GET | Retrieves customer contacts from Unleashed by customer. |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [Create Product](actions/create-product.md) | POST | Creates a new product in Unleashed. |
| [Get Product](actions/get-product.md) | GET | Retrieves a product from your Unleashed inventory catalog. |
| [List Products](actions/list-products.md) | GET | Retrieves products from your Unleashed inventory catalog. |
| [Update Product](actions/update-product.md) | PUT | Updates an existing product in Unleashed. |

### Purchase Order

| Action | Method | Description |
| --- | --- | --- |
| [Create Purchase Order](actions/create-purchase-order.md) | POST | Creates a new purchase order in Unleashed. |
| [Delete Purchase Order](actions/delete-purchase-order.md) | DELETE | Deletes an existing purchase order from Unleashed. |
| [Get Purchase Order](actions/get-purchase-order.md) | GET | Retrieves a purchase order from your Unleashed account. |
| [List Purchase Orders](actions/list-purchase-orders.md) | GET | Retrieves purchase orders from your Unleashed account. |
| [Update Purchase Order](actions/update-purchase-order.md) | PUT | Updates an existing purchase order in Unleashed. |

### Sales Order

| Action | Method | Description |
| --- | --- | --- |
| [Create Sales Order](actions/create-sales-order.md) | POST | Creates a new sales order in Unleashed. |
| [Delete Sales Order](actions/delete-sales-order.md) | DELETE | Deletes an existing sales order from Unleashed. |
| [Get Sales Order](actions/get-sales-order.md) | GET | Retrieves a sales order from your Unleashed account. |
| [List Sales Orders](actions/list-sales-orders.md) | GET | Retrieves sales orders from your Unleashed account. |
| [Update Sales Order](actions/update-sales-order.md) | PUT | Updates an existing sales order in Unleashed. |

### Sales Shipment

| Action | Method | Description |
| --- | --- | --- |
| [Create Sales Shipment](actions/create-sales-shipment.md) | POST | Creates a new sales shipment in Unleashed. |
| [Delete Sales Shipment](actions/delete-sales-shipment.md) | DELETE | Deletes an existing sales shipment from Unleashed. |
| [Get Sales Shipment](actions/get-sales-shipment.md) | GET | Retrieves a sales shipment from your Unleashed account. |
| [List Sales Shipments](actions/list-sales-shipments.md) | GET | Retrieves sales shipments from your Unleashed account. |
| [Update Sales Shipment](actions/update-sales-shipment.md) | PUT | Updates an existing sales shipment in Unleashed. |

### Stock On Hand

| Action | Method | Description |
| --- | --- | --- |
| [List Stock On Hand](actions/list-stock-on-hand.md) | GET | Retrieves stock-on-hand records from your Unleashed account. |

### Supplier

| Action | Method | Description |
| --- | --- | --- |
| [List Suppliers](actions/list-suppliers.md) | GET | Retrieves suppliers from your Unleashed supplier directory. |

### Warehouse

| Action | Method | Description |
| --- | --- | --- |
| [List Warehouses](actions/list-warehouses.md) | GET | Retrieves warehouses from your Unleashed account. |


# <img src="https://images.mindcloud.co/apps/icons/ido-af-snu-en-logos_1775077249213.jpeg" alt="Stockpilot logo" width="28" height="28"> Stockpilot: Universal API

Manage inventory, products, orders, and sales channels

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/stockpilot/latest
- **Category:** Commerce
- **Actions:** 35
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://stockpilot.com
- **Vendor API docs:** https://api.stockpilot.dev/redoc

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Verify API Credentials](actions/verify-api-credentials.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stockpilot/latest/actions/verify-api-credentials?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (35)

### Brand

| Action | Method | Description |
| --- | --- | --- |
| [Create Brand](actions/create-brand.md) | POST | Creates a new brand in Stockpilot. |
| [List Brands](actions/list-brands.md) | GET | Retrieves brands from Stockpilot. |

### Category

| Action | Method | Description |
| --- | --- | --- |
| [Create Category](actions/create-category.md) | POST | Creates a new category in Stockpilot. |
| [List Categories](actions/list-categories.md) | GET | Retrieves categories from Stockpilot. |

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [List Customers](actions/list-customers.md) | GET | Retrieves customers from Stockpilot. |

### Inventory Item

| Action | Method | Description |
| --- | --- | --- |
| [Create Inventory Item](actions/create-inventory-item.md) | POST | Creates a new inventory item in Stockpilot. |
| [Get Inventory Item](actions/get-inventory-item.md) | GET | Retrieves an inventory item from Stockpilot. |
| [List Inventory Items](actions/list-inventory-items.md) | GET | Retrieves inventory items from Stockpilot. |
| [Update Inventory Item](actions/update-inventory-item.md) | PUT | Updates an existing inventory item in Stockpilot. |

### Invoice

| Action | Method | Description |
| --- | --- | --- |
| [Send Invoice](actions/send-invoice.md) | POST | Sends an invoice for an order in Stockpilot. |

### Invoices

| Action | Method | Description |
| --- | --- | --- |
| [Get Invoice for Order](actions/get-invoice-for-order.md) | GET | Retrieves an invoice for an order in Stockpilot. |

### Items

| Action | Method | Description |
| --- | --- | --- |
| [Update Ordered Item Details](actions/update-ordered-item-details.md) | PUT | Updates an ordered item in Stockpilot. |

### Metrics

| Action | Method | Description |
| --- | --- | --- |
| [Get Item Sales Analytics](actions/get-item-sales-analytics.md) | GET | Retrieves item sales analytics from Stockpilot. |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [Create Order](actions/create-order.md) | POST | Creates a new order in Stockpilot. |
| [Fulfil Order](actions/fulfil-order.md) | PUT | Updates an order as fulfilled in Stockpilot. |

### Orders

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Order](actions/cancel-order.md) | PUT | Updates an order as canceled in Stockpilot. |
| [Delete Entire Order](actions/delete-entire-order.md) | DELETE | Deletes an order from Stockpilot. |
| [Get Single Order](actions/get-single-order.md) | GET | Retrieves an order from Stockpilot. |
| [List Orders](actions/list-orders.md) | GET | Retrieves orders from Stockpilot. |
| [List Orders with Cancellation Requests](actions/list-orders-with-cancellation-requests.md) | GET | Retrieves orders with cancellation requests from Stockpilot. |
| [Update Order Status](actions/update-order-status.md) | PUT | Updates an order status in Stockpilot. |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [Verify API Credentials](actions/verify-api-credentials.md) | GET | Retrieves organization details for the current Stockpilot credentials. |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [Create Product](actions/create-product.md) | POST | Creates a new product in Stockpilot. |
| [Get Product by ID](actions/get-product-by-id.md) | GET | Retrieves a product from Stockpilot. |
| [List Products](actions/list-products.md) | GET | Retrieves products from Stockpilot. |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Get Sales Summary](actions/get-sales-summary.md) | GET | Retrieves sales summary analytics from Stockpilot. |

### Sales Channel

| Action | Method | Description |
| --- | --- | --- |
| [List Sales Channels](actions/list-sales-channels.md) | GET | Retrieves sales channels from Stockpilot. |

### Shipments

| Action | Method | Description |
| --- | --- | --- |
| [Get Fulfillment Details](actions/get-fulfillment-details.md) | GET | Retrieves fulfillment details for an order in Stockpilot. |
| [Get Label Suggestion](actions/get-label-suggestion.md) | GET | Retrieves shipping label suggestions from Stockpilot. |
| [List Shipping Integrations](actions/list-shipping-integrations.md) | GET | Retrieves shipping integrations from Stockpilot. |
| [Request Shipping Label](actions/request-shipping-label.md) | POST | Requests a shipping label in Stockpilot. |
| [Retrieve Shipping Label](actions/retrieve-shipping-label.md) | GET | Retrieves a shipping label from Stockpilot. |

### Supplier

| Action | Method | Description |
| --- | --- | --- |
| [List Suppliers](actions/list-suppliers.md) | GET | Retrieves suppliers from Stockpilot. |

### Warehouse

| Action | Method | Description |
| --- | --- | --- |
| [List Warehouses](actions/list-warehouses.md) | GET | Retrieves warehouses from Stockpilot. |

### Warehouse Item

| Action | Method | Description |
| --- | --- | --- |
| [List Warehouse Items](actions/list-warehouse-items.md) | GET | Retrieves inventory items from a Stockpilot warehouse. |


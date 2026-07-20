# <img src="https://images.mindcloud.co/apps/icons/hiboutik_1775157884580.png" alt="Hiboutik logo" width="28" height="28"> Hiboutik: Universal API

Hiboutik is a cloud point-of-sale platform for retail and hospitality businesses. Use this app to manage catalog data, customers, inventory, sales, kitchen operations, reporting, and store settings through the Hiboutik REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/hiboutik/latest
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.hiboutik.com/
- **Vendor API docs:** https://mindcloudhiboutik20260402.hiboutik.com/docapi/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Brands](actions/list-brands.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hiboutik/latest/actions/list-brands?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Brand

| Action | Method | Description |
| --- | --- | --- |
| [List Brands](actions/list-brands.md) | GET | Retrieves product brands from Hiboutik. |

### Calendar Event

| Action | Method | Description |
| --- | --- | --- |
| [Get Calendar Event](actions/get-calendar-event.md) | GET | Retrieves a calendar event from Hiboutik. |
| [List Calendar Events](actions/list-calendar-events.md) | GET | Retrieves calendar events for a specific date in Hiboutik. |

### Category

| Action | Method | Description |
| --- | --- | --- |
| [List Categories](actions/list-categories.md) | GET | Retrieves product categories from Hiboutik. |

### Cooking Station

| Action | Method | Description |
| --- | --- | --- |
| [List Kitchen Cooking Stations](actions/list-kitchen-cooking-stations.md) | GET | Retrieves kitchen cooking stations from Hiboutik. |

### Credit Note

| Action | Method | Description |
| --- | --- | --- |
| [List Pending Credit Notes](actions/list-pending-credit-notes.md) | GET | Retrieves pending credit notes for a store in Hiboutik. |

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [Get Customer](actions/get-customer.md) | GET | Retrieves a customer from Hiboutik. |
| [List Customers](actions/list-customers.md) | GET | Retrieves customers from Hiboutik. |

### Customer Address

| Action | Method | Description |
| --- | --- | --- |
| [Get Customer Address](actions/get-customer-address.md) | GET | Retrieves a customer address from Hiboutik. |

### Kitchen Sale

| Action | Method | Description |
| --- | --- | --- |
| [List Kitchen Open Tables](actions/list-kitchen-open-tables.md) | GET | Retrieves pending kitchen sales from Hiboutik. |

### Modifier

| Action | Method | Description |
| --- | --- | --- |
| [List Modifiers](actions/list-modifiers.md) | GET | Retrieves modifiers from Hiboutik. |

### Payment Type

| Action | Method | Description |
| --- | --- | --- |
| [List Payment Types](actions/list-payment-types.md) | GET | Retrieves payment types for a store in Hiboutik. |

### Prepaid Purchase

| Action | Method | Description |
| --- | --- | --- |
| [List Customer Prepaid Purchase Lines](actions/list-customer-prepaid-purchase-lines.md) | GET | Retrieves prepaid purchase lines for a customer in Hiboutik. |
| [List Prepaid Purchase Lines](actions/list-prepaid-purchase-lines.md) | GET | Retrieves prepaid purchase lines from Hiboutik. |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [Get Product](actions/get-product.md) | GET | Retrieves a product from Hiboutik. |
| [List Products](actions/list-products.md) | GET | Retrieves products from Hiboutik. |
| [Search Products By Barcode](actions/search-products-by-barcode.md) | GET | Finds products in Hiboutik by barcode. |
| [Search Products By Name](actions/search-products-by-name.md) | GET | Finds products in Hiboutik by name. |

### Product Barcode

| Action | Method | Description |
| --- | --- | --- |
| [Get Product Barcode](actions/get-product-barcode.md) | GET | Retrieves a product barcode from Hiboutik. |

### Product Purchase History

| Action | Method | Description |
| --- | --- | --- |
| [List Product Purchased History](actions/list-product-purchased-history.md) | GET | Retrieves purchased product history from Hiboutik. |

### Products Purchased Report

| Action | Method | Description |
| --- | --- | --- |
| [List Products Purchased](actions/list-products-purchased.md) | GET | Retrieves purchased products for a specific date in Hiboutik. |

### Products Returned Report

| Action | Method | Description |
| --- | --- | --- |
| [List Products Returned](actions/list-products-returned.md) | GET | Retrieves returned products for a specific date in Hiboutik. |

### Products Sold Report

| Action | Method | Description |
| --- | --- | --- |
| [List Products Sold](actions/list-products-sold.md) | GET | Retrieves products sold for a specific date in Hiboutik. |

### Sale

| Action | Method | Description |
| --- | --- | --- |
| [Get First Closed Sale](actions/get-first-closed-sale.md) | GET | Retrieves the first closed sale for a store in Hiboutik. |
| [Get Sale](actions/get-sale.md) | GET | Retrieves a sale from Hiboutik. |
| [List Closed Sales](actions/list-closed-sales.md) | GET | Retrieves closed sales for a specific date in Hiboutik. |
| [List Open Sales](actions/list-open-sales.md) | GET | Retrieves open sales for a store in Hiboutik. |

### Stock Order

| Action | Method | Description |
| --- | --- | --- |
| [Get Stock Order](actions/get-stock-order.md) | GET | Retrieves a stock order from Hiboutik. |
| [List Stock Orders](actions/list-stock-orders.md) | GET | Retrieves stock orders from Hiboutik. |

### Stock Order Line

| Action | Method | Description |
| --- | --- | --- |
| [List Stock Order Details](actions/list-stock-order-details.md) | GET | Retrieves stock order details from Hiboutik. |
| [List Stock Order Details on Hold](actions/list-stock-order-details-on-hold.md) | GET | Retrieves on-hold stock order details from Hiboutik. |

### Stock Transfer

| Action | Method | Description |
| --- | --- | --- |
| [Get Stock Transfer](actions/get-stock-transfer.md) | GET | Retrieves a stock transfer from Hiboutik. |
| [List Stock Transfers](actions/list-stock-transfers.md) | GET | Retrieves stock transfers from Hiboutik. |

### Stock Transfer Line

| Action | Method | Description |
| --- | --- | --- |
| [List Stock Transfer Details](actions/list-stock-transfer-details.md) | GET | Retrieves stock transfer details from Hiboutik. |

### Store

| Action | Method | Description |
| --- | --- | --- |
| [List Stores](actions/list-stores.md) | GET | Retrieves stores from Hiboutik. |

### Subscription

| Action | Method | Description |
| --- | --- | --- |
| [List Subscriptions](actions/list-subscriptions.md) | GET | Retrieves subscriptions from Hiboutik. |

### Supplier

| Action | Method | Description |
| --- | --- | --- |
| [List Suppliers](actions/list-suppliers.md) | GET | Retrieves suppliers from Hiboutik. |

### Tax

| Action | Method | Description |
| --- | --- | --- |
| [List Taxes](actions/list-taxes.md) | GET | Retrieves tax rates from Hiboutik. |

### Till Movement

| Action | Method | Description |
| --- | --- | --- |
| [List Cash Movements](actions/list-cash-movements.md) | GET | Retrieves monthly cash movements for a store in Hiboutik. |

### Warehouse

| Action | Method | Description |
| --- | --- | --- |
| [List Warehouses](actions/list-warehouses.md) | GET | Retrieves warehouses from Hiboutik. |


# <img src="https://images.mindcloud.co/apps/icons/order-sender_1775734331251.png" alt="Order Sender logo" width="28" height="28"> Order Sender: Universal API

Order Sender Business API wrapper for exporting, importing, and deleting business data such as orders, products, customers, suppliers, discounts, quotes, and price lists.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/orderSender/latest
- **Actions:** 28
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://developer.ordersender.com/
- **Vendor API docs:** https://developer.ordersender.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Verify Connection](actions/verify-connection.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/orderSender/latest/actions/verify-connection?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (28)

### Commission

| Action | Method | Description |
| --- | --- | --- |
| [Import Commissions](actions/import-commissions.md) | POST | Imports commission records into Order Sender. |
| [List Commissions](actions/list-commissions.md) | GET | Retrieves commission records from Order Sender. |

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Verify Connection](actions/verify-connection.md) | GET | Retrieves Order Sender account status and API access validity. |

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [Delete Customers](actions/delete-customers.md) | DELETE | Deletes customer records from Order Sender. |
| [Import Customers](actions/import-customers.md) | POST | Imports customer records into Order Sender. |
| [List Customers](actions/list-customers.md) | GET | Retrieves customer records from Order Sender. |

### Customer Payment Condition

| Action | Method | Description |
| --- | --- | --- |
| [Import Customer Payment Conditions](actions/import-customer-payment-conditions.md) | POST | Imports customer payment conditions into Order Sender. |
| [List Customer Payment Conditions](actions/list-customer-payment-conditions.md) | GET | Retrieves customer payment conditions from Order Sender. |

### Discount

| Action | Method | Description |
| --- | --- | --- |
| [Delete Discounts](actions/delete-discounts.md) | DELETE | Deletes discount records from Order Sender. |
| [Import Discounts](actions/import-discounts.md) | POST | Imports discount records into Order Sender. |
| [List Discounts](actions/list-discounts.md) | GET | Retrieves discount records from Order Sender. |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [List Orders](actions/list-orders.md) | GET | Retrieves sales orders from Order Sender. |

### Payment Condition

| Action | Method | Description |
| --- | --- | --- |
| [Delete Payment Conditions](actions/delete-payment-conditions.md) | DELETE | Deletes payment conditions from Order Sender. |
| [Import Payment Conditions](actions/import-payment-conditions.md) | POST | Imports payment conditions into Order Sender. |
| [List Payment Conditions](actions/list-payment-conditions.md) | GET | Retrieves payment conditions from Order Sender. |

### Price List

| Action | Method | Description |
| --- | --- | --- |
| [Import Price Lists](actions/import-price-lists.md) | POST | Imports price lists into Order Sender. |
| [List Price Lists](actions/list-price-lists.md) | GET | Retrieves price lists from Order Sender. |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [Delete Products](actions/delete-products.md) | DELETE | Deletes product records from Order Sender. |
| [Import Products](actions/import-products.md) | POST | Imports product records into Order Sender. |
| [List Products](actions/list-products.md) | GET | Retrieves product records from Order Sender. |

### Prospect

| Action | Method | Description |
| --- | --- | --- |
| [Delete Prospects](actions/delete-prospects.md) | DELETE | Deletes prospect records from Order Sender. |
| [Import Prospects](actions/import-prospects.md) | POST | Imports prospect records into Order Sender. |
| [List Prospects](actions/list-prospects.md) | GET | Retrieves prospect records from Order Sender. |

### Quote

| Action | Method | Description |
| --- | --- | --- |
| [List Quotes](actions/list-quotes.md) | GET | Retrieves sales quotes from Order Sender. |

### Secondary Address

| Action | Method | Description |
| --- | --- | --- |
| [Delete Secondary Addresses](actions/delete-secondary-addresses.md) | DELETE | Deletes secondary addresses from Order Sender. |
| [Import Secondary Addresses](actions/import-secondary-addresses.md) | POST | Imports secondary addresses into Order Sender. |

### Supplier

| Action | Method | Description |
| --- | --- | --- |
| [Import Suppliers](actions/import-suppliers.md) | POST | Imports supplier records into Order Sender. |
| [List Suppliers](actions/list-suppliers.md) | GET | Retrieves supplier records from Order Sender. |


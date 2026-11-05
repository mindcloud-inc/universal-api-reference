# <img src="https://images.mindcloud.co/apps/icons/sf-logo_1774370260627.png" alt="Salesforce logo" width="28" height="28"> Salesforce: Universal API

Salesforce through the MindCloud Universal API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/salesForce/latest
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Contacts](actions/get-contacts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salesForce/latest/actions/get-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | POST |  |
| [Get Contact by Email](actions/get-contact-by-email.md) | GET |  |
| [Get Contacts](actions/get-contacts.md) | GET |  |

### Credit Memos

| Action | Method | Description |
| --- | --- | --- |
| [List Credit Memos](actions/list-credit-memos.md) | GET |  |

### Credit Notes

| Action | Method | Description |
| --- | --- | --- |
| [List Billing Credit Notes](actions/list-billing-credit-notes.md) | GET |  |

### CRM Accounts

| Action | Method | Description |
| --- | --- | --- |
| [Create Account](actions/create-account.md) | POST |  |

### Fulfillments

| Action | Method | Description |
| --- | --- | --- |
| [Get Fulfillment Orders](actions/get-fulfillment-orders.md) | GET |  |

### Invoices

| Action | Method | Description |
| --- | --- | --- |
| [List Billing Invoices](actions/list-billing-invoices.md) | GET |  |
| [List Invoices](actions/list-invoices.md) | GET |  |

### Order Delivery Group

| Action | Method | Description |
| --- | --- | --- |
| [Get Order Delivery Group](actions/get-order-delivery-group.md) | GET |  |

### Order Delivery Method

| Action | Method | Description |
| --- | --- | --- |
| [Get Order Delivery Method](actions/get-order-delivery-method.md) | GET |  |

### Price Books

| Action | Method | Description |
| --- | --- | --- |
| [List Pricebook](actions/list-pricebook.md) | GET |  |

### Pricebook Entry

| Action | Method | Description |
| --- | --- | --- |
| [List Pricebook Entry](actions/list-pricebook-entry.md) | GET |  |

### Products

| Action | Method | Description |
| --- | --- | --- |
| [Create Product](actions/create-product.md) | POST |  |
| [Find Product Offer by Product Code](actions/find-product-by-product-code.md) | GET |  |
| [Update Product](actions/update-product.md) | PUT |  |

### Quote Lines

| Action | Method | Description |
| --- | --- | --- |
| [Get Deleted Quote Line Items](actions/get-deleted-quote-line-items.md) | GET |  |
| [List Quote Line Items](actions/list-quote-line-items.md) | GET |  |

### Quotes

| Action | Method | Description |
| --- | --- | --- |
| [List Quotes](actions/list-quotes.md) | GET |  |

### Record

| Action | Method | Description |
| --- | --- | --- |
| [Create Record](actions/create-record.md) | POST |  |
| [Delete Record](actions/delete-record.md) | DELETE |  |
| [Update Record](actions/update-recordv2.md) | PUT |  |

### Sales Order Lines

| Action | Method | Description |
| --- | --- | --- |
| [Create Order Item](actions/create-order-item.md) | POST |  |
| [Update Order Items](actions/update-invoice.md) | PUT |  |

### Sales Orders

| Action | Method | Description |
| --- | --- | --- |
| [Create Order](actions/create-order.md) | POST |  |
| [Find Order by OrderNumber](actions/get-order.md) | GET | Get the ID for a single Order object by its Order Number |
| [List Orders](actions/list-orders.md) | GET |  |

### Sobject

| Action | Method | Description |
| --- | --- | --- |
| [Org sObjects (Lookup)](actions/lookup-s-objects.md) | GET | Returns the authenticated organizations sObjects for Lookup fields. |

### Soql Query

| Action | Method | Description |
| --- | --- | --- |
| [Query (SOQL)](actions/query.md) | GET | Use raw SOQL syntax to Query your Salesforce Org. |
| [Query Order Items (test)](actions/query-order-items-test.md) | GET |  |


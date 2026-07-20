# <img src="https://images.mindcloud.co/apps/icons/agiliron_1775071795307.png" alt="Agiliron logo" width="28" height="28"> Agiliron: Universal API

Agiliron is an omnichannel commerce and business management platform for inventory, orders, CRM, and fulfillment operations.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/agiliron/latest
- **Category:** Commerce
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.agiliron.com
- **Vendor API docs:** https://api.agiliron.com/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Read Contact](actions/read-contact.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/agiliron/latest/actions/read-contact?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Add Account](actions/add-account.md) | POST | Creates a new account in Agiliron. |
| [Read Account](actions/read-account.md) | GET | Retrieves account records from Agiliron. |
| [Update Account](actions/update-account.md) | PUT | Updates an existing account in Agiliron. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Add Contact](actions/add-contact.md) | POST | Creates a new contact in Agiliron. |
| [Read Contact](actions/read-contact.md) | GET | Retrieves contact records from Agiliron. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in Agiliron. |

### Inventories

| Action | Method | Description |
| --- | --- | --- |
| [Add Product Inventory](actions/add-product-inventory.md) | POST | Adds inventory to an existing product in Agiliron. |
| [Read Product Inventory](actions/read-product-inventory.md) | GET | Retrieves product inventory records from Agiliron. |

### Leads

| Action | Method | Description |
| --- | --- | --- |
| [Add Lead](actions/add-lead.md) | POST | Creates a new lead in Agiliron. |
| [Read Lead](actions/read-lead.md) | GET | Retrieves lead records from Agiliron. |
| [Update Lead](actions/update-lead.md) | PUT | Updates an existing lead in Agiliron. |

### Products

| Action | Method | Description |
| --- | --- | --- |
| [Add Product](actions/add-product.md) | POST | Creates a new product in Agiliron. |
| [Read Product](actions/read-product.md) | GET | Retrieves product records from Agiliron. |
| [Update Product](actions/update-product.md) | PUT | Updates an existing product in Agiliron. |

### Purchase Orders

| Action | Method | Description |
| --- | --- | --- |
| [Add PurchaseOrder](actions/add-purchase-order.md) | POST | Creates a new purchase order in Agiliron. |
| [Read PurchaseOrder](actions/read-purchase-order.md) | GET | Retrieves purchase order records from Agiliron. |
| [Update PurchaseOrder](actions/update-purchase-order.md) | PUT | Updates an existing purchase order in Agiliron. |

### Quotes

| Action | Method | Description |
| --- | --- | --- |
| [Add Quote](actions/add-quote.md) | POST | Creates a new quote in Agiliron. |
| [Read Quote](actions/read-quote.md) | GET | Retrieves quote records from Agiliron. |

### Sales Orders

| Action | Method | Description |
| --- | --- | --- |
| [Add SalesOrder](actions/add-sales-order.md) | POST | Creates a new sales order in Agiliron. |
| [Read SalesOrder](actions/read-sales-order.md) | GET | Retrieves sales order records from Agiliron. |
| [Update SalesOrder](actions/update-sales-order.md) | PUT | Updates an existing sales order in Agiliron. |

### Vendors

| Action | Method | Description |
| --- | --- | --- |
| [Add Vendor](actions/add-vendor.md) | POST | Creates a new vendor in Agiliron. |
| [Read Vendor](actions/read-vendor.md) | GET | Retrieves vendor records from Agiliron. |


# <img src="https://images.mindcloud.co/apps/icons/zoho-inventory_1773673837048.png" alt="Zoho Inventory logo" width="28" height="28"> Zoho Inventory: Universal API

Manage inventory catalog, contacts, sales orders, packages, shipments, and invoices

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/zohoInventory/latest
- **Category:** Commerce
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.zoho.com/inventory/
- **Vendor API docs:** https://www.zoho.com/inventory/api/v1/introduction/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Organizations](actions/list-organizations.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoInventory/latest/actions/list-organizations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in Zoho Inventory. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from Zoho Inventory. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from Zoho Inventory. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in Zoho Inventory. |

### Invoice

| Action | Method | Description |
| --- | --- | --- |
| [Create Invoice](actions/create-invoice.md) | POST | Creates a new invoice in Zoho Inventory. |
| [Get Invoice](actions/get-invoice.md) | GET | Retrieves an invoice from Zoho Inventory. |
| [List Invoices](actions/list-invoices.md) | GET | Retrieves invoices from Zoho Inventory. |
| [Update Invoice](actions/update-invoice.md) | PUT | Updates an existing invoice in Zoho Inventory. |

### Item

| Action | Method | Description |
| --- | --- | --- |
| [Create Item](actions/create-item.md) | POST | Creates a new item in Zoho Inventory. |
| [Get Item](actions/get-item.md) | GET | Retrieves an item from Zoho Inventory. |
| [List Items](actions/list-items.md) | GET | Retrieves items from Zoho Inventory. |
| [Update Item](actions/update-item.md) | PUT | Updates an existing item in Zoho Inventory. |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [List Organizations](actions/list-organizations.md) | GET | Retrieves organizations from Zoho Inventory. |

### Package

| Action | Method | Description |
| --- | --- | --- |
| [Create Package](actions/create-package.md) | POST | Creates a new package in Zoho Inventory. |
| [Get Package](actions/get-package.md) | GET | Retrieves a package from Zoho Inventory. |
| [List Packages](actions/list-packages.md) | GET | Retrieves packages from Zoho Inventory. |

### Sales Order

| Action | Method | Description |
| --- | --- | --- |
| [Confirm Sales Order](actions/confirm-sales-order.md) | PUT | Marks a sales order as confirmed in Zoho Inventory. |
| [Create Sales Order](actions/create-sales-order.md) | POST | Creates a new sales order in Zoho Inventory. |
| [Get Sales Order](actions/get-sales-order.md) | GET | Retrieves a sales order from Zoho Inventory. |
| [List Sales Orders](actions/list-sales-orders.md) | GET | Retrieves sales orders from Zoho Inventory. |
| [Update Sales Order](actions/update-sales-order.md) | PUT | Updates an existing sales order in Zoho Inventory. |

### Shipment Order

| Action | Method | Description |
| --- | --- | --- |
| [Create Shipment Order](actions/create-shipment-order.md) | POST | Creates a new shipment order in Zoho Inventory. |
| [Get Shipment Order](actions/get-shipment-order.md) | GET | Retrieves a shipment order from Zoho Inventory. |
| [Mark Shipment Order Delivered](actions/mark-shipment-order-delivered.md) | PUT | Marks a shipment order as delivered in Zoho Inventory. |


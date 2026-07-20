# <img src="https://images.mindcloud.co/apps/icons/images-4_1773421937523.png" alt="Loyverse logo" width="28" height="28"> Loyverse: Universal API

Loyverse: Manage retail items, inventory, receipts, and customers

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/loyverse/latest
- **Category:** Commerce
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://loyverse.com
- **Vendor API docs:** https://developer.loyverse.com/docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Items](actions/list-items.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/loyverse/latest/actions/list-items?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Category

| Action | Method | Description |
| --- | --- | --- |
| [Create or Update Category](actions/create-or-update-category.md) | PUT | Creates or updates a category in Loyverse. |
| [Delete Category](actions/delete-category.md) | DELETE | Deletes an existing category from Loyverse. |
| [Get Category](actions/get-category.md) | GET | Retrieves a category record from Loyverse. |
| [List Categories](actions/list-categories.md) | GET | Retrieves category records from the Loyverse catalog. |

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [Create or Update Customer](actions/create-or-update-customer.md) | PUT | Creates or updates a customer in Loyverse. |
| [Delete Customer](actions/delete-customer.md) | DELETE | Deletes an existing customer from Loyverse. |
| [Get Customer](actions/get-customer.md) | GET | Retrieves a customer record from Loyverse. |
| [List Customers](actions/list-customers.md) | GET | Retrieves customer records from the Loyverse database. |

### Inventory Level

| Action | Method | Description |
| --- | --- | --- |
| [Batch Update Inventory Levels](actions/batch-update-inventory-levels.md) | PUT | Updates inventory levels in batch in Loyverse. |
| [List Inventory Levels](actions/list-inventory-levels.md) | GET | Retrieves current inventory levels from Loyverse. |

### Item

| Action | Method | Description |
| --- | --- | --- |
| [Create or Update Item](actions/create-or-update-item.md) | PUT | Creates or updates an item in Loyverse. |
| [Delete Item](actions/delete-item.md) | DELETE | Deletes an existing item from Loyverse. |
| [Get Item](actions/get-item.md) | GET | Retrieves an item record from Loyverse. |
| [List Items](actions/list-items.md) | GET | Retrieves item records from the Loyverse catalog. |

### Receipt

| Action | Method | Description |
| --- | --- | --- |
| [Create Sales Receipt](actions/create-sales-receipt.md) | POST | Creates a new sales receipt in Loyverse. |
| [Get Receipt](actions/get-receipt.md) | GET | Retrieves a sales receipt from Loyverse. |
| [List Receipts](actions/list-receipts.md) | GET | Retrieves sales receipt records from Loyverse. |

### Refund Receipt

| Action | Method | Description |
| --- | --- | --- |
| [Create Refund Receipt](actions/create-refund-receipt.md) | POST | Creates a refund receipt in Loyverse. |

### Shift

| Action | Method | Description |
| --- | --- | --- |
| [Get Shift](actions/get-shift.md) | GET | Retrieves a shift record from Loyverse. |
| [List Shifts](actions/list-shifts.md) | GET | Retrieves shift records from the Loyverse account. |

### Store

| Action | Method | Description |
| --- | --- | --- |
| [Get Store](actions/get-store.md) | GET | Retrieves a store record from Loyverse. |
| [List Stores](actions/list-stores.md) | GET | Retrieves store records from the Loyverse account. |

### Supplier

| Action | Method | Description |
| --- | --- | --- |
| [Create or Update Supplier](actions/create-or-update-supplier.md) | PUT | Creates or updates a supplier in Loyverse. |
| [Delete Supplier](actions/delete-supplier.md) | DELETE | Deletes an existing supplier from Loyverse. |
| [Get Supplier](actions/get-supplier.md) | GET | Retrieves a supplier record from Loyverse. |
| [List Suppliers](actions/list-suppliers.md) | GET | Retrieves supplier records from the Loyverse account. |

### Variant

| Action | Method | Description |
| --- | --- | --- |
| [Create or Update Variant](actions/create-or-update-variant.md) | PUT | Creates or updates a product variant in Loyverse. |
| [Delete Variant](actions/delete-variant.md) | DELETE | Deletes an existing product variant from Loyverse. |
| [Get Variant](actions/get-variant.md) | GET | Retrieves a product variant from Loyverse. |
| [List Variants](actions/list-variants.md) | GET | Retrieves product variant records from Loyverse. |


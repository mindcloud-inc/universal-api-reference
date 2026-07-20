# <img src="https://images.mindcloud.co/apps/icons/net-suite_1780348776698.png" alt="NetSuite - Basic logo" width="28" height="28"> NetSuite - Basic: Universal API

Connect to Oracle NetSuite SuiteTalk REST Web Services for core ERP, CRM, sales, purchasing, billing, and lookup records.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/netSuiteBasic/latest
- **Category:** Commerce / Accounting
- **Actions:** 99
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.netsuite.com/
- **Vendor API docs:** https://docs.oracle.com/en/cloud/saas/netsuite/ns-online-help/chapter_1540391670.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Accounts](actions/list-accounts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/netSuiteBasic/latest/actions/list-accounts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (99)

### Accounting Periods

| Action | Method | Description |
| --- | --- | --- |
| [List Accounting Periods](actions/list-accounting-periods.md) | GET | Retrieves a list of accounting periods from NetSuite. |

### Accounts

| Action | Method | Description |
| --- | --- | --- |
| [List Accounts](actions/list-accounts.md) | GET | Retrieves a list of accounts from NetSuite. |

### Bills

| Action | Method | Description |
| --- | --- | --- |
| [Get Vendor Bill](actions/get-vendor-bill.md) | GET | Retrieves details for the vendor bill in NetSuite. |
| [List Vendor Bills](actions/list-vendor-bills.md) | GET | Retrieves a list of vendor bills from NetSuite. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Get Contact](actions/get-contact.md) | GET | Retrieves details for the contact in NetSuite. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves a list of contacts from NetSuite. |

### Coupons

| Action | Method | Description |
| --- | --- | --- |
| [List Promotion Codes](actions/list-promotion-codes.md) | GET | Retrieves a list of promotion codes from NetSuite. |

### Credit Notes

| Action | Method | Description |
| --- | --- | --- |
| [List Credit Memos](actions/list-credit-memos.md) | GET | Retrieves a list of credit memos from NetSuite. |

### Custom Record

| Action | Method | Description |
| --- | --- | --- |
| [List Custom Records](actions/list-custom-records.md) | GET | Retrieves a list of custom records from NetSuite. |

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [Get Customer](actions/get-customer.md) | GET | Retrieves details for the customer in NetSuite. |
| [List Customers](actions/list-customers.md) | GET | Retrieves a list of customers from NetSuite. |

### Customization

| Action | Method | Description |
| --- | --- | --- |
| [List Record Fields](actions/list-record-fields.md) | GET | Retrieves a list of record fields from NetSuite. |
| [Test Connection](actions/test-connection.md) | GET | Tests whether the NetSuite connection is working. |

### Departments

| Action | Method | Description |
| --- | --- | --- |
| [List Departments](actions/list-departments.md) | GET | Retrieves a list of departments from NetSuite. |

### Employees

| Action | Method | Description |
| --- | --- | --- |
| [List Employees](actions/list-employees.md) | GET | Retrieves a list of employees from NetSuite. |

### Fulfillments

| Action | Method | Description |
| --- | --- | --- |
| [List Item Fulfillments](actions/list-item-fulfillments.md) | GET | Retrieves a list of item fulfillments from NetSuite. |

### Goods Receipts

| Action | Method | Description |
| --- | --- | --- |
| [List Item Receipts](actions/list-item-receipts.md) | GET | Retrieves a list of item receipts from NetSuite. |

### Inventories

| Action | Method | Description |
| --- | --- | --- |
| [List Inventory Numbers](actions/list-inventory-numbers.md) | GET | Retrieves a list of inventory numbers from NetSuite. |

### Invoices

| Action | Method | Description |
| --- | --- | --- |
| [Get Invoice](actions/get-invoice.md) | GET | Retrieves details for the invoice in NetSuite. |
| [List Invoices](actions/list-invoices.md) | GET | Retrieves a list of invoices from NetSuite. |

### Item Fulfillment

| Action | Method | Description |
| --- | --- | --- |
| [List Service Items](actions/list-service-items.md) | GET | Retrieves a list of service items from NetSuite. |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves a list of tasks from NetSuite. |
| [List Time Bills](actions/list-time-bills.md) | GET | Retrieves a list of time bills from NetSuite. |

### Items

| Action | Method | Description |
| --- | --- | --- |
| [Get Inventory Item](actions/get-inventory-item.md) | GET | Retrieves details for the inventory item in NetSuite. |
| [Get Non-Inventory Sale Item](actions/get-non-inventory-sale-item.md) | GET | Retrieves details for the non-inventory sale item in NetSuite. |
| [List Assembly Items](actions/list-assembly-items.md) | GET | Retrieves a list of assembly items from NetSuite. |
| [List Group Items](actions/list-group-items.md) | GET | Retrieves a list of group items from NetSuite. |
| [List Inventory Items](actions/list-inventory-items.md) | GET | Retrieves a list of inventory items from NetSuite. |
| [List Lot Numbered Assembly Items](actions/list-lot-numbered-assembly-items.md) | GET | Retrieves a list of lot numbered assembly items from NetSuite. |
| [List Lot Numbered Inventory Items](actions/list-lot-numbered-inventory-items.md) | GET | Retrieves a list of lot numbered inventory items from NetSuite. |
| [List Non-Inventory Items](actions/list-non-inventory-items.md) | GET | Retrieves a list of non-inventory items from NetSuite. |
| [List Non-Inventory Sale Items](actions/list-non-inventory-sale-items.md) | GET | Retrieves a list of non-inventory sale items from NetSuite. |
| [List Other Charge Items](actions/list-other-charge-items.md) | GET | Retrieves a list of other charge items from NetSuite. |
| [List Serialized Assembly Items](actions/list-serialized-assembly-items.md) | GET | Retrieves a list of serialized assembly items from NetSuite. |
| [List Serialized Inventory Items](actions/list-serialized-inventory-items.md) | GET | Retrieves a list of serialized inventory items from NetSuite. |

### Locations

| Action | Method | Description |
| --- | --- | --- |
| [List Locations](actions/list-locations.md) | GET | Retrieves a list of locations from NetSuite. |

### Metadata

| Action | Method | Description |
| --- | --- | --- |
| [Get Record Types](actions/get-record-types.md) | GET | Retrieves details for the record types in NetSuite. |

### Opportunities

| Action | Method | Description |
| --- | --- | --- |
| [List Opportunities](actions/list-opportunities.md) | GET | Retrieves a list of opportunities from NetSuite. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Create Account](actions/create-account.md) | POST | Creates a new account in NetSuite. |
| [Create Classification](actions/create-classification.md) | POST | Creates a new classification in NetSuite. |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in NetSuite. |
| [Create Customer](actions/create-customer.md) | POST | Creates a new customer in NetSuite. |
| [Create Employee](actions/create-employee.md) | POST | Creates a new employee in NetSuite. |
| [Create Location](actions/create-location.md) | POST | Creates a new location in NetSuite. |
| [Create Purchase Order](actions/create-purchase-order.md) | POST | Creates a new purchase order in NetSuite. |
| [Create Term](actions/create-term.md) | POST | Creates a new term in NetSuite. |
| [Create Time Bill](actions/create-time-bill.md) | POST | Creates a new time bill in NetSuite. |
| [Create Vendor](actions/create-vendor.md) | POST | Creates a new vendor in NetSuite. |
| [Create Vendor Bill](actions/create-vendor-bill.md) | POST | Creates a new vendor bill in NetSuite. |
| [Delete Account](actions/delete-account.md) | DELETE | Deletes an existing account from NetSuite. |
| [Delete Classification](actions/delete-classification.md) | DELETE | Deletes an existing classification from NetSuite. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes an existing contact from NetSuite. |
| [Delete Customer](actions/delete-customer.md) | DELETE | Deletes an existing customer from NetSuite. |
| [Delete Employee](actions/delete-employee.md) | DELETE | Deletes an existing employee from NetSuite. |
| [Delete Location](actions/delete-location.md) | DELETE | Deletes an existing location from NetSuite. |
| [Delete Purchase Order](actions/delete-purchase-order.md) | DELETE | Deletes an existing purchase order from NetSuite. |
| [Delete Term](actions/delete-term.md) | DELETE | Deletes an existing term from NetSuite. |
| [Delete Time Bill](actions/delete-time-bill.md) | DELETE | Deletes an existing time bill from NetSuite. |
| [Delete Vendor](actions/delete-vendor.md) | DELETE | Deletes an existing vendor from NetSuite. |
| [Delete Vendor Bill](actions/delete-vendor-bill.md) | DELETE | Deletes an existing vendor bill from NetSuite. |
| [Update Account](actions/update-account.md) | PUT | Updates an existing account in NetSuite. |
| [Update Classification](actions/update-classification.md) | PUT | Updates an existing classification in NetSuite. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in NetSuite. |
| [Update Customer](actions/update-customer.md) | PUT | Updates an existing customer in NetSuite. |
| [Update Employee](actions/update-employee.md) | PUT | Updates an existing employee in NetSuite. |
| [Update Location](actions/update-location.md) | PUT | Updates an existing location in NetSuite. |
| [Update Purchase Order](actions/update-purchase-order.md) | PUT | Updates an existing purchase order in NetSuite. |
| [Update Term](actions/update-term.md) | PUT | Updates an existing term in NetSuite. |
| [Update Time Bill](actions/update-time-bill.md) | PUT | Updates an existing time bill in NetSuite. |
| [Update Vendor](actions/update-vendor.md) | PUT | Updates an existing vendor in NetSuite. |
| [Update Vendor Bill](actions/update-vendor-bill.md) | PUT | Updates an existing vendor bill in NetSuite. |

### Payment Methods

| Action | Method | Description |
| --- | --- | --- |
| [List Payment Methods](actions/list-payment-methods.md) | GET | Retrieves a list of payment methods from NetSuite. |

### Payments

| Action | Method | Description |
| --- | --- | --- |
| [List Customer Deposits](actions/list-customer-deposits.md) | GET | Retrieves a list of customer deposits from NetSuite. |
| [List Customer Payments](actions/list-customer-payments.md) | GET | Retrieves a list of customer payments from NetSuite. |

### Purchase Orders

| Action | Method | Description |
| --- | --- | --- |
| [Get Purchase Order](actions/get-purchase-order.md) | GET | Retrieves details for the purchase order in NetSuite. |
| [List Purchase Orders](actions/list-purchase-orders.md) | GET | Retrieves a list of purchase orders from NetSuite. |

### Refunds

| Action | Method | Description |
| --- | --- | --- |
| [List Cash Refunds](actions/list-cash-refunds.md) | GET | Retrieves a list of cash refunds from NetSuite. |
| [List Customer Refunds](actions/list-customer-refunds.md) | GET | Retrieves a list of customer refunds from NetSuite. |

### Returns

| Action | Method | Description |
| --- | --- | --- |
| [List Return Authorizations](actions/list-return-authorizations.md) | GET | Retrieves a list of return authorizations from NetSuite. |

### Sales Orders

| Action | Method | Description |
| --- | --- | --- |
| [Get Sales Order](actions/get-sales-order.md) | GET | Retrieves details for the sales order in NetSuite. |
| [List Sales Orders](actions/list-sales-orders.md) | GET | Retrieves a list of sales orders from NetSuite. |

### Search

| Action | Method | Description |
| --- | --- | --- |
| [Get Record Fields](actions/get-record-fields.md) | GET | Retrieves details for the record fields in NetSuite. |
| [Search using SuiteQL](actions/search-using-suite-ql.md) | GET | Finds NetSuite records using a SuiteQL query. |

### Shipments

| Action | Method | Description |
| --- | --- | --- |
| [List Inbound Shipments](actions/list-inbound-shipments.md) | GET | Retrieves a list of inbound shipments from NetSuite. |

### Shipping Item

| Action | Method | Description |
| --- | --- | --- |
| [List Shipping Items](actions/list-shipping-items.md) | GET | Retrieves a list of shipping items from NetSuite. |

### Stock Movements

| Action | Method | Description |
| --- | --- | --- |
| [List Inventory Adjustments](actions/list-inventory-adjustments.md) | GET | Retrieves a list of inventory adjustments from NetSuite. |

### Subsidiaries

| Action | Method | Description |
| --- | --- | --- |
| [List Subsidiaries](actions/list-subsidiaries.md) | GET | Retrieves a list of subsidiaries from NetSuite. |

### Term

| Action | Method | Description |
| --- | --- | --- |
| [List Terms](actions/list-terms.md) | GET | Retrieves a list of terms from NetSuite. |

### Tracking Categories

| Action | Method | Description |
| --- | --- | --- |
| [List Classifications](actions/list-classifications.md) | GET | Retrieves a list of classifications from NetSuite. |

### Transactions

| Action | Method | Description |
| --- | --- | --- |
| [Get Estimate](actions/get-estimate.md) | GET | Retrieves details for the estimate in NetSuite. |
| [List Cash Sales](actions/list-cash-sales.md) | GET | Retrieves a list of cash sales from NetSuite. |
| [List Estimates](actions/list-estimates.md) | GET | Retrieves a list of estimates from NetSuite. |

### Transfer Order

| Action | Method | Description |
| --- | --- | --- |
| [List Transfer Orders](actions/list-transfer-orders.md) | GET | Retrieves a list of transfer orders from NetSuite. |

### Vendor Bill

| Action | Method | Description |
| --- | --- | --- |
| [List Vendor Credits](actions/list-vendor-credits.md) | GET | Retrieves a list of vendor credits from NetSuite. |

### Vendor Return Authorization

| Action | Method | Description |
| --- | --- | --- |
| [List Vendor Return Authorizations](actions/list-vendor-return-authorizations.md) | GET | Retrieves a list of vendor return authorizations from NetSuite. |

### Vendors

| Action | Method | Description |
| --- | --- | --- |
| [Get Vendor](actions/get-vendor.md) | GET | Retrieves details for the vendor in NetSuite. |
| [List Vendors](actions/list-vendors.md) | GET | Retrieves a list of vendors from NetSuite. |

### Warehouses

| Action | Method | Description |
| --- | --- | --- |
| [List Bin Numbers](actions/list-bin-numbers.md) | GET | Retrieves a list of bin numbers from NetSuite. |

### Work Order

| Action | Method | Description |
| --- | --- | --- |
| [List Work Orders](actions/list-work-orders.md) | GET | Retrieves a list of work orders from NetSuite. |


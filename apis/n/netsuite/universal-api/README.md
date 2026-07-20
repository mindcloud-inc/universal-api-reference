# <img src="https://images.mindcloud.co/apps/icons/ns-logo_1772827092529.png" alt="NetSuite - Advanced logo" width="28" height="28"> NetSuite - Advanced: Universal API

Leading integrated cloud business software suite, including business accounting, ERP, CRM and e-commerce software.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/netsuite/latest
- **Category:** Marketing
- **Actions:** 180
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.netsuite.com/portal/home.shtml
- **Vendor API docs:** https://docs.oracle.com/en/cloud/saas/netsuite/ns-online-help/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Items](actions/get-assembly-items.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/netsuite/latest/actions/get-assembly-items?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (180)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Create Account](actions/create-account.md) | POST |  |
| [List Accounts](actions/list-accounts.md) | GET |  |
| [Update Account](actions/update-account.md) | PUT |  |

### Accounting Period

| Action | Method | Description |
| --- | --- | --- |
| [List Accounting Periods](actions/list-accounting-periods.md) | GET |  |

### Bin Number

| Action | Method | Description |
| --- | --- | --- |
| [List Bin Numbers](actions/list-bin-numbers.md) | GET |  |

### Cash Sale

| Action | Method | Description |
| --- | --- | --- |
| [Create Cash Sale](actions/create-cash-sale.md) | POST |  |
| [Delete Cash Sale](actions/delete-cash-sale.md) | DELETE |  |
| [List Cash Sales](actions/list-cash-sales.md) | GET |  |
| [Update Cash Sale](actions/update-cash-sale.md) | PUT |  |

### Classification

| Action | Method | Description |
| --- | --- | --- |
| [Delete Assembly Item](actions/delete-assembly-item.md) | DELETE |  |
| [Delete Classification](actions/delete-classification.md) | DELETE |  |
| [Delete Group Item](actions/delete-group-item.md) | DELETE |  |
| [Delete Inventory Item](actions/delete-inventory-item.md) | DELETE |  |
| [Delete Item](actions/delete-item.md) | DELETE |  |
| [Delete Location](actions/delete-location.md) | DELETE |  |
| [Delete Lot Numbered Assembly Item](actions/delete-lot-numbered-assembly-item.md) | DELETE |  |
| [Delete Lot Numbered Inventory Item](actions/delete-lot-numbered-inventory-item.md) | DELETE |  |
| [Delete Non-Inventory Item](actions/delete-non-inventory-item.md) | DELETE |  |
| [Delete Other Charge Item](actions/delete-other-charge-item.md) | DELETE |  |
| [Delete Serialized Assembly Item](actions/delete-serialized-assembly-item.md) | DELETE |  |
| [Delete Serialized Inventory Item](actions/delete-serialized-inventory-item.md) | DELETE |  |
| [Delete Service Item](actions/delete-service-item.md) | DELETE |  |
| [List Classifications](actions/list-classifications.md) | GET |  |
| [Update Classification](actions/update-classification.md) | PUT |  |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Delete Contact](actions/delete-contact.md) | DELETE |  |

### Credit Memo

| Action | Method | Description |
| --- | --- | --- |
| [Create Credit Memo](actions/create-credit-memo.md) | POST |  |
| [Delete Credit Memo](actions/delete-credit-memo.md) | DELETE |  |
| [List Credit Memos](actions/list-credit-memos.md) | GET |  |
| [Update Credit Memo](actions/update-credit-memo.md) | PUT |  |

### Custom

| Action | Method | Description |
| --- | --- | --- |
| [Create Custom Record](actions/create-custom-record.md) | POST |  |

### Custom Record

| Action | Method | Description |
| --- | --- | --- |
| [Delete Custom Record](actions/delete-custom-record.md) | DELETE |  |
| [List Custom Records](actions/list-custom-records.md) | GET |  |
| [Update Custom Record](actions/update-custom-record.md) | PUT |  |

### Customer Refund

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer Refund](actions/create-customer-refund.md) | POST |  |
| [Delete Customer Refund](actions/delete-customer-refund.md) | DELETE |  |
| [List Customer Refunds](actions/list-customer-refunds.md) | GET |  |
| [Update Customer Refund](actions/update-customer-refund.md) | PUT |  |

### Customization

| Action | Method | Description |
| --- | --- | --- |
| [Execute Custom Code](actions/execute-custom-code.md) | PUT | Execute custom code using the SuiteScript scripting language |
| [List Record Fields](actions/list-record-fields.md) | GET |  |

### Deposit

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer Deposit](actions/create-customer-deposit.md) | POST |  |
| [Create Deposit](actions/create-deposit.md) | POST |  |
| [Delete Customer Deposit](actions/delete-customer-deposit.md) | DELETE |  |
| [List Customer Deposits](actions/list-customer-deposits.md) | GET |  |
| [Update Customer Deposit](actions/update-customer-deposit.md) | PUT |  |

### Inventory Adjustment

| Action | Method | Description |
| --- | --- | --- |
| [Create Inventory Adjustment](actions/create-inventory-adjustment.md) | POST |  |
| [Delete Inventory Adjustment](actions/delete-inventory-adjustment.md) | DELETE |  |
| [List Inventory Adjustments](actions/list-inventory-adjustments.md) | GET |  |
| [Update Inventory Adjustment](actions/update-inventory-adjustment.md) | PUT |  |
| [Update Vendor Return Authorization](actions/update-vendor-return-authorization.md) | PUT |  |

### Item Fulfillment

| Action | Method | Description |
| --- | --- | --- |
| [Create Assembly Item](actions/create-assembly-item.md) | POST |  |
| [Create Contact](actions/create-contact.md) | POST |  |
| [Create Customer](actions/create-customer.md) | POST |  |
| [Create Customer Payment](actions/create-customer-payment.md) | POST |  |
| [Create Employee](actions/create-employee.md) | POST |  |
| [Create Group Item](actions/create-group-item.md) | POST |  |
| [Create Inventory Item](actions/create-inventory-item.md) | POST |  |
| [Create Invoice](actions/create-invoice.md) | POST |  |
| [Create Item Fulfillment](actions/create-item-fulfillment.md) | POST | Item Fulfillment is a record that says, “We shipped these items to the customer.” It’s how NetSuite keeps track of what was sent out from a… |
| [Create Lot Numbered Assembly Item](actions/create-lot-numbered-assembly-item.md) | POST |  |
| [Create Lot Numbered Inventory Item](actions/create-lot-numbered-inventory-item.md) | POST |  |
| [Create Non-Inventory Item](actions/create-non-inventory-item.md) | POST |  |
| [Create Other Charge Item](actions/create-other-charge-item.md) | POST |  |
| [Create Project](actions/create-project.md) | POST |  |
| [Create Project Task](actions/create-project-task.md) | POST |  |
| [Create Purchase Order](actions/create-purchase-order.md) | POST |  |
| [Create Sales Order](actions/create-sales-order.md) | POST |  |
| [Create Serialized Assembly Item](actions/create-serialized-assembly-item.md) | POST |  |
| [Create Serialized Inventory Item](actions/create-serialized-inventory-item.md) | POST |  |
| [Create Service Item](actions/create-service-item.md) | POST |  |
| [Create Term](actions/create-term.md) | POST |  |
| [Create Time Bill](actions/create-time-bill.md) | POST |  |
| [Create Vendor](actions/create-vendor.md) | POST |  |
| [Create Vendor Return Authorization](actions/create-vendor-return-authorization.md) | POST |  |
| [Delete Account](actions/delete-account.md) | DELETE |  |
| [Delete Customer](actions/delete-customer.md) | DELETE |  |
| [Delete Customer Payment](actions/delete-customer-payment.md) | DELETE |  |
| [Delete Invoice](actions/delete-invoice.md) | DELETE |  |
| [Delete Item Fulfillment](actions/delete-item-fulfillment.md) | DELETE |  |
| [Delete Purchase Order](actions/delete-purchase-order.md) | DELETE |  |
| [Delete Sales Order](actions/delete-sales-order.md) | DELETE |  |
| [Delete Term](actions/delete-term.md) | DELETE |  |
| [Delete Vendor](actions/delete-vendor.md) | DELETE |  |
| [List Items](actions/get-assembly-items.md) | GET |  |
| [List Assembly Items](actions/list-assembly-items.md) | GET |  |
| [List Contacts](actions/list-contacts.md) | GET |  |
| [List Customer Payments](actions/list-customer-payments.md) | GET |  |
| [List Customers](actions/list-customers.md) | GET |  |
| [List Departments](actions/list-departments.md) | GET |  |
| [List Employees](actions/list-employees.md) | GET |  |
| [List Files](actions/list-files.md) | GET |  |
| [List Group Items](actions/list-group-items.md) | GET |  |
| [List Inventory Items](actions/list-inventory-items.md) | GET |  |
| [List Inventory Numbers](actions/list-inventory-numbers.md) | GET |  |
| [List Invoices](actions/list-invoices.md) | GET |  |
| [List Item Fulfillments](actions/list-item-fulfillments.md) | GET | Item Fulfillment is a record that says, “We shipped these items to the customer.” It’s how NetSuite keeps track of what was sent out from a… |
| [List Lot Numbered Assembly Items](actions/list-lot-numbered-assembly-items.md) | GET |  |
| [List Lot Numbered Inventory Items](actions/list-lot-numbered-inventory-items.md) | GET |  |
| [List Non-Inventory Items](actions/list-non-inventory-items.md) | GET |  |
| [List Opportunities](actions/list-opportunities.md) | GET |  |
| [List Other Charge Items](actions/list-other-charge-items.md) | GET |  |
| [List Payment Methods](actions/list-payment-methods.md) | GET |  |
| [List Project Tasks](actions/list-project-tasks.md) | GET |  |
| [List Projects](actions/list-projects.md) | GET |  |
| [List Purchase Orders](actions/list-purchase-orders.md) | GET |  |
| [List Sales Orders](actions/list-sales-orders.md) | GET |  |
| [List Serialized Assembly Items](actions/list-serialized-assembly-items.md) | GET |  |
| [List Serialized Inventory Items](actions/list-serialized-inventory-items.md) | GET |  |
| [List Service Items](actions/list-service-items.md) | GET |  |
| [List Tasks](actions/list-tasks.md) | GET |  |
| [List Time Bills](actions/list-time-bills.md) | GET |  |
| [List Vendors](actions/list-vendors.md) | GET |  |
| [Update Assembly Item](actions/update-assembly-item.md) | PUT |  |
| [Update Contact](actions/update-contact.md) | PUT |  |
| [Update Customer](actions/update-customer.md) | PUT |  |
| [Update Customer Payment](actions/update-customer-payment.md) | PUT |  |
| [Update Employee](actions/update-employee.md) | PUT |  |
| [Update Group Item](actions/update-group-item.md) | PUT |  |
| [Update Inventory Item](actions/update-inventory-item.md) | PUT |  |
| [Update Invoice](actions/update-invoice.md) | PUT |  |
| [Update Item Fulfillments](actions/update-item-fulfillments.md) | PUT | Item Fulfillment is a record that says, “We shipped these items to the customer.” It’s how NetSuite keeps track of what was sent out from a… |
| [Update Lot Numbered Assembly Item](actions/update-lot-numbered-assembly-item.md) | PUT |  |
| [Update Lot Numbered Inventory Item](actions/update-lot-numbered-inventory-item.md) | PUT |  |
| [Update Non-Inventory Item](actions/update-non-inventory-item.md) | PUT |  |
| [Update Term](actions/update-other-change-item.md) | PUT |  |
| [Update Other Charge Item](actions/update-other-charge-item.md) | PUT |  |
| [Update Project](actions/update-project.md) | PUT |  |
| [Update Project Task](actions/update-project-task.md) | PUT |  |
| [Update Purchase Order](actions/update-purchase-order.md) | PUT |  |
| [Update Sales Order](actions/update-sales-order.md) | PUT |  |
| [Update Serialized Assembly Item](actions/update-serialized-assembly-item.md) | PUT |  |
| [Update Serialized Inventory Item](actions/update-serialized-inventory-item.md) | PUT |  |
| [Update Service Item](actions/update-service-item.md) | PUT |  |
| [Update Time Bill](actions/update-time-bill.md) | PUT |  |
| [Update Vendor](actions/update-vendor.md) | PUT |  |

### Item Receipt

| Action | Method | Description |
| --- | --- | --- |
| [Create Item Receipt](actions/create-item-receipt.md) | POST |  |
| [Delete Item Receipt](actions/delete-item-receipt.md) | DELETE |  |
| [List Item Receipts](actions/list-item-receipts.md) | GET |  |
| [Update Item Receipt](actions/update-item-receipt.md) | PUT |  |

### Location

| Action | Method | Description |
| --- | --- | --- |
| [Create Location](actions/create-location.md) | POST |  |
| [List Locations](actions/list-locations.md) | GET |  |
| [Update Location](actions/update-location.md) | PUT |  |

### Promotion Code

| Action | Method | Description |
| --- | --- | --- |
| [Create Promotion Code](actions/create-promotion-code.md) | POST |  |
| [Delete Accounting Period](actions/delete-accounting-period.md) | DELETE |  |
| [Delete Employee](actions/delete-employee.md) | DELETE |  |
| [Delete File](actions/delete-file.md) | DELETE |  |
| [Delete Project](actions/delete-project.md) | DELETE |  |
| [Delete Project Task](actions/delete-project-task.md) | DELETE |  |
| [Delete Promotion Code](actions/delete-promotion-code.md) | DELETE |  |
| [Delete Time Bill](actions/delete-time-bill.md) | DELETE |  |
| [List Promotion Codes](actions/list-promotion-codes.md) | GET |  |
| [Update Promotion Code](actions/update-promotion-code.md) | PUT |  |

### Refund

| Action | Method | Description |
| --- | --- | --- |
| [Create Cash Refund](actions/create-cash-refund.md) | POST |  |
| [Delete Cash Refund](actions/delete-cash-refund.md) | DELETE |  |
| [Delete Shipping Item](actions/delete-shipping-item.md) | DELETE |  |
| [List Cash Refunds](actions/list-cash-refunds.md) | GET |  |
| [Update Cash Refund](actions/update-cash-refund.md) | PUT |  |

### Return Authorization

| Action | Method | Description |
| --- | --- | --- |
| [List Return Authorizations](actions/list-return-authorizations.md) | GET |  |
| [Update Return Authorization](actions/update-return-authorization.md) | PUT |  |

### Search

| Action | Method | Description |
| --- | --- | --- |
| [Get Restlet](actions/get-restlet.md) | GET |  |
| [Search using Saved Search](actions/get-saved-search.md) | GET | Search using a previously saved search using NetSuite's Query Language |

### Shipment

| Action | Method | Description |
| --- | --- | --- |
| [List Inbound Shipments](actions/list-inbound-shipments.md) | GET |  |

### Shipping Item

| Action | Method | Description |
| --- | --- | --- |
| [Create Shipping Item](actions/create-shipping-item.md) | POST |  |
| [List Shipping Items](actions/list-shipping-items.md) | GET |  |
| [Update Shipping Item](actions/update-shipping-item.md) | PUT |  |

### State

| Action | Method | Description |
| --- | --- | --- |
| [List States](actions/list-states.md) | GET |  |

### Subsidiary

| Action | Method | Description |
| --- | --- | --- |
| [List Subsidiaries](actions/list-subsidiaries.md) | GET |  |

### Term

| Action | Method | Description |
| --- | --- | --- |
| [List Terms](actions/list-terms.md) | GET |  |

### Transfer Order

| Action | Method | Description |
| --- | --- | --- |
| [Delete Transfer Order](actions/delete-transfer-order.md) | DELETE |  |
| [List Transfer Orders](actions/list-transfer-orders.md) | GET |  |
| [Update Transfer Order](actions/update-transfer-order.md) | PUT |  |

### Vendor Bill

| Action | Method | Description |
| --- | --- | --- |
| [Delete Vendor Bill](actions/delete-vendor-bill.md) | DELETE |  |
| [Delete Vendor Credit](actions/delete-vendor-credit.md) | DELETE |  |
| [List Vendor Bills](actions/list-vendor-bills.md) | GET |  |
| [List Vendor Credits](actions/list-vendor-credits.md) | GET |  |
| [Update Vendor Bill](actions/update-vendor-bill.md) | PUT |  |
| [Update Vendor Credit](actions/update-vendor-credit.md) | PUT |  |

### Vendor Return Authorization

| Action | Method | Description |
| --- | --- | --- |
| [List Vendor Return Authorizations](actions/list-vendor-return-authorizations.md) | GET |  |

### Work Order

| Action | Method | Description |
| --- | --- | --- |
| [Create Work Order](actions/create-work-order.md) | POST |  |
| [List Work Orders](actions/list-work-orders.md) | GET |  |
| [Update Work Order](actions/update-work-order.md) | PUT |  |


# NetSuite - Advanced Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model NetSuite - Advanced expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/netsuite/latest/actions/get-assembly-items?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## NetSuite - Advanced actions that support pagination

- [Delete Vendor Credit](actions/delete-vendor-credit.md)
- [Execute Custom Code](actions/execute-custom-code.md)
- [List Items](actions/get-assembly-items.md)
- [Search using Saved Search](actions/get-saved-search.md)
- [List Accounting Periods](actions/list-accounting-periods.md)
- [List Accounts](actions/list-accounts.md)
- [List Assembly Items](actions/list-assembly-items.md)
- [List Bin Numbers](actions/list-bin-numbers.md)
- [List Cash Refunds](actions/list-cash-refunds.md)
- [List Cash Sales](actions/list-cash-sales.md)
- [List Classifications](actions/list-classifications.md)
- [List Contacts](actions/list-contacts.md)
- [List Credit Memos](actions/list-credit-memos.md)
- [List Custom Records](actions/list-custom-records.md)
- [List Customer Deposits](actions/list-customer-deposits.md)
- [List Customer Payments](actions/list-customer-payments.md)
- [List Customer Refunds](actions/list-customer-refunds.md)
- [List Customers](actions/list-customers.md)
- [List Departments](actions/list-departments.md)
- [List Employees](actions/list-employees.md)
- [List Files](actions/list-files.md)
- [List Group Items](actions/list-group-items.md)
- [List Inbound Shipments](actions/list-inbound-shipments.md)
- [List Inventory Adjustments](actions/list-inventory-adjustments.md)
- [List Inventory Items](actions/list-inventory-items.md)
- [List Inventory Numbers](actions/list-inventory-numbers.md)
- [List Invoices](actions/list-invoices.md)
- [List Item Fulfillments](actions/list-item-fulfillments.md)
- [List Item Receipts](actions/list-item-receipts.md)
- [List Locations](actions/list-locations.md)
- [List Lot Numbered Assembly Items](actions/list-lot-numbered-assembly-items.md)
- [List Lot Numbered Inventory Items](actions/list-lot-numbered-inventory-items.md)
- [List Non-Inventory Items](actions/list-non-inventory-items.md)
- [List Opportunities](actions/list-opportunities.md)
- [List Other Charge Items](actions/list-other-charge-items.md)
- [List Payment Methods](actions/list-payment-methods.md)
- [List Project Tasks](actions/list-project-tasks.md)
- [List Projects](actions/list-projects.md)
- [List Promotion Codes](actions/list-promotion-codes.md)
- [List Purchase Orders](actions/list-purchase-orders.md)
- [List Record Fields](actions/list-record-fields.md)
- [List Return Authorizations](actions/list-return-authorizations.md)
- [List Sales Orders](actions/list-sales-orders.md)
- [List Serialized Assembly Items](actions/list-serialized-assembly-items.md)
- [List Serialized Inventory Items](actions/list-serialized-inventory-items.md)
- [List Service Items](actions/list-service-items.md)
- [List Shipping Items](actions/list-shipping-items.md)
- [List States](actions/list-states.md)
- [List Subsidiaries](actions/list-subsidiaries.md)
- [List Tasks](actions/list-tasks.md)
- [List Terms](actions/list-terms.md)
- [List Time Bills](actions/list-time-bills.md)
- [List Transfer Orders](actions/list-transfer-orders.md)
- [List Vendor Bills](actions/list-vendor-bills.md)
- [List Vendor Credits](actions/list-vendor-credits.md)
- [List Vendor Return Authorizations](actions/list-vendor-return-authorizations.md)
- [List Vendors](actions/list-vendors.md)
- [List Work Orders](actions/list-work-orders.md)

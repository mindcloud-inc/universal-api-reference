# SAP ERP (S/4HANA) Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model SAP ERP (S/4HANA) expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sAPERPS4HANA/latest/actions/list-customer-companies?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## SAP ERP (S/4HANA) actions that support pagination

- [List Customer Companies](actions/list-customer-companies.md)
- [List Customer Sales Area Taxes](actions/list-customer-sales-area-taxes.md)
- [List Customer Sales Areas](actions/list-customer-sales-areas.md)
- [List Customer Sales Partner Functions](actions/list-customer-sales-partner-functions.md)
- [List Customers](actions/list-customers.md)
- [List Supplier Companies](actions/list-supplier-companies.md)
- [List Supplier Partner Functions](actions/list-supplier-partner-functions.md)
- [List Supplier Purchasing Organizations](actions/list-supplier-purchasing-organizations.md)
- [List Supplier Withholding Taxes](actions/list-supplier-withholding-taxes.md)
- [List Suppliers](actions/list-suppliers.md)

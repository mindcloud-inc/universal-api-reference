# Microsoft Dynamics 365 BC Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Microsoft Dynamics 365 BC expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoftDynamics365BC/latest/actions/create-credit-memo-itens-o-data-v4?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Microsoft Dynamics 365 BC actions that support pagination

- [Create Credit Memo Itens ODataV4](actions/create-credit-memo-itens-o-data-v4.md)
- [Get Inventory By Location SSI](actions/get-inventory-by-location-ssi.md)
- [List Bank Deposits Line ODataV4](actions/list-bank-deposits-line-o-data-v4.md)
- [List Bank Deposits ODataV4](actions/list-bank-deposits-o-data-v4.md)
- [List Companies](actions/list-companies.md)
- [List Credit Memo ODataV4](actions/list-credit-memo-o-data-v4.md)
- [List Customer Ledger Entries ODataV4](actions/list-customer-ledger-entries-o-data-v4.md)
- [List Customers](actions/list-customers.md)
- [List Customers ODataV4](actions/list-customers-o-data-v4.md)
- [List Customers SSI](actions/list-customers-ssi.md)
- [List Employees ODataV4](actions/list-employees-o-data-v4.md)
- [List General Journal ODataV4](actions/list-general-journal-o-data-v4.md)
- [List Items](actions/list-items.md)
- [List Journal Lines Payments ODataV4](actions/list-journal-lines-payments-o-data-v4.md)
- [List Payroll Journal ODataV4](actions/list-payroll-journal-o-data-v4.md)
- [List Projects](actions/list-projects.md)
- [List Sales Invoice](actions/list-sales-invoice.md)
- [List Sales Invoice Line Items](actions/list-sales-invoice-line-items.md)
- [List Sales Invoice ODataV4](actions/list-sales-invoice-o-data-v4.md)
- [List Sales Orders SSI](actions/list-sales-orders-ssi.md)

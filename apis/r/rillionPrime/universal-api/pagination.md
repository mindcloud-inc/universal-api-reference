# Rillion Prime Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Rillion Prime expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/get-invoice-account-coding-history?connectionId=$CONNECTION_ID&limit=25&offset=0&invoiceId=1&role=Administrator" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Rillion Prime actions that support pagination

- [Get Invoice Account Coding History](actions/get-invoice-account-coding-history.md)
- [List Accounts By Role](actions/list-accounts-by-role.md)
- [List Allocation Types For Role](actions/list-allocation-types-for-role.md)
- [List Asset Types For Role](actions/list-asset-types-for-role.md)
- [List Assets By Role](actions/list-assets-by-role.md)
- [List Companies By Role](actions/list-companies-by-role.md)
- [List Currencies](actions/list-currencies.md)
- [List Flow Proposal For Role](actions/list-flow-proposal-for-role.md)
- [List Invoice Queue](actions/list-invoice-queue.md)
- [List Invoices](actions/list-invoices.md)
- [List Locked Rows](actions/list-locked-rows.md)
- [List Object Relation](actions/list-object-relation.md)
- [List Object Relation Setting](actions/list-object-relation-setting.md)
- [List Objects For Role](actions/list-objects-for-role.md)
- [List Payment Audit Logs](actions/list-payment-audit-logs.md)
- [List Payment Suppliers](actions/list-payment-suppliers.md)
- [List Payments](actions/list-payments.md)
- [List Periods For Role](actions/list-periods-for-role.md)
- [List Roles](actions/list-roles.md)
- [List Suppliers For Role](actions/list-suppliers-for-role.md)
- [List VAT Codes For Role](actions/list-vat-codes-for-role.md)
- [Search For Expenditures](actions/search-for-expenditures.md)

# Avalara AvaTax Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Avalara AvaTax expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/avalara/latest/actions/list-countries?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Avalara AvaTax actions that support pagination

- [List Countries](actions/list-countries.md)
- [List Currencies](actions/list-currencies.md)
- [List Entity Use Codes](actions/list-entity-use-codes.md)
- [List Items By Company](actions/list-items-by-company.md)
- [List Jurisdictions Hierarchy](actions/list-jurisdictions-hierarchy.md)
- [List Nexus By Company](actions/list-nexus-by-company.md)
- [List Parameters](actions/list-parameters.md)
- [List Tax Authority Types](actions/list-tax-authority-types.md)
- [List Tax Code Types](actions/list-tax-code-types.md)
- [List Tax Codes By Company](actions/list-tax-codes-by-company.md)
- [List Tax Rules](actions/list-tax-rules.md)
- [List Transactions By Company](actions/list-transactions-by-company.md)
- [Query Companies](actions/query-companies.md)
- [Query Customers](actions/query-customers.md)
- [Query Tax Codes](actions/query-tax-codes.md)

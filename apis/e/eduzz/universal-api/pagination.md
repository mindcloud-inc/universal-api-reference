# Eduzz Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Eduzz expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eduzz/latest/actions/get-financial-statement?connectionId=$CONNECTION_ID&limit=25&offset=0&endDate=2026-03-18&startDate=2024-01-01" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Eduzz actions that support pagination

- [Get Financial Statement](actions/get-financial-statement.md)
- [List Affiliates](actions/list-affiliates.md)
- [List Chargebacks](actions/list-chargebacks.md)
- [List Customers](actions/list-customers.md)
- [List Products](actions/list-products.md)
- [List Sales](actions/list-sales.md)
- [List Students](actions/list-students.md)
- [List Transfers](actions/list-transfers.md)

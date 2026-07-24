# Rillion Prime Pay Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Rillion Prime Pay expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/list-payment-audit-logs?connectionId=$CONNECTION_ID&limit=25&offset=0&searchReferenceId=RillionPay2&referenceType=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Rillion Prime Pay actions that support pagination

- [List Payment Audit Logs](actions/list-payment-audit-logs.md)
- [List Payment Suppliers](actions/list-payment-suppliers.md)
- [List Payments](actions/list-payments.md)

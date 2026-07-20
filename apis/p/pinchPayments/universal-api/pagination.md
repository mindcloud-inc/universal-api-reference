# Pinch Payments Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Pinch Payments expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pinchPayments/latest/actions/list-events?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Pinch Payments actions that support pagination

- [List Events](actions/list-events.md)
- [List Payers](actions/list-payers.md)
- [List Payment Links](actions/list-payment-links.md)
- [List Payment Links for Payer](actions/list-payment-links-for-payer.md)
- [List Processed Payments](actions/list-processed-payments.md)
- [List Refunds](actions/list-refunds.md)
- [List Scheduled Payments](actions/list-scheduled-payments.md)

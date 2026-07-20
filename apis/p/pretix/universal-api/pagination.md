# pretix Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model pretix expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pretix/latest/actions/list-check-in-lists?connectionId=$CONNECTION_ID&limit=25&offset=0&organizer=string&event=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## pretix actions that support pagination

- [List Check In Lists](actions/list-check-in-lists.md)
- [List Events](actions/list-events.md)
- [List Invoices](actions/list-invoices.md)
- [List Item Variations](actions/list-item-variations.md)
- [List Items](actions/list-items.md)
- [List Order Positions](actions/list-order-positions.md)
- [List Orders](actions/list-orders.md)
- [List Organizers](actions/list-organizers.md)
- [List Quotas](actions/list-quotas.md)
- [List Sub Events](actions/list-sub-events.md)
- [List Vouchers](actions/list-vouchers.md)
- [Search Organizer Orders](actions/search-organizer-orders.md)

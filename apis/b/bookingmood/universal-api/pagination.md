# Bookingmood Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Bookingmood expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bookingmood/latest/actions/list-bookings?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Bookingmood actions that support pagination

- [List Bookings](actions/list-bookings.md)
- [List Calendar Events](actions/list-calendar-events.md)
- [List Contacts](actions/list-contacts.md)
- [List Invoices](actions/list-invoices.md)
- [List Messages](actions/list-messages.md)
- [List Payments](actions/list-payments.md)
- [List Products](actions/list-products.md)
- [List Sites](actions/list-sites.md)

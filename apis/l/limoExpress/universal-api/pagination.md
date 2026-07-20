# LimoExpress Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model LimoExpress expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/limoExpress/latest/actions/list-all-currencies?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## LimoExpress actions that support pagination

- [List All Currencies](actions/list-all-currencies.md)
- [List Booking Offers](actions/list-booking-offers.md)
- [List Bookings](actions/list-bookings.md)
- [List Clients](actions/list-clients.md)
- [List Countries](actions/list-countries.md)
- [List Expenses](actions/list-expenses.md)
- [List Invoices](actions/list-invoices.md)
- [List Passengers](actions/list-passengers.md)
- [List Payment Methods](actions/list-payment-methods.md)
- [List Users](actions/list-users.md)
- [List Vehicle Classes](actions/list-vehicle-classes.md)
- [List Vehicles](actions/list-vehicles.md)

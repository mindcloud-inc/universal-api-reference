# Understory Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Understory expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/understory/latest/actions/list-bookings?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Understory actions that support pagination

- [List Bookings](actions/list-bookings.md)
- [List Event Availability](actions/list-event-availability.md)
- [List Events](actions/list-events.md)
- [List Experiences](actions/list-experiences.md)
- [List Information Requests](actions/list-information-requests.md)
- [List Marketing Consents](actions/list-marketing-consents.md)
- [List Orders](actions/list-orders.md)
- [List Ticket Variants](actions/list-ticket-variants.md)
- [List Webhook Subscriptions](actions/list-webhook-subscriptions.md)

# Ticket Tailor Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Ticket Tailor expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ticketTailor/latest/actions/list-check-ins?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Ticket Tailor actions that support pagination

- [List Check Ins](actions/list-check-ins.md)
- [List Checkout Form Elements](actions/list-checkout-form-elements.md)
- [List Checkout Forms](actions/list-checkout-forms.md)
- [List Discounts](actions/list-discounts.md)
- [List Event Occurrences](actions/list-event-occurrences.md)
- [List Event Series](actions/list-event-series.md)
- [List Events](actions/list-events.md)
- [List Holds](actions/list-holds.md)
- [List Issued Tickets](actions/list-issued-tickets.md)
- [List Orders](actions/list-orders.md)
- [List Products](actions/list-products.md)
- [List Stores](actions/list-stores.md)

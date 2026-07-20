# Customer.io Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Customer.io expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/customerio/latest/actions/list-customer-messages?connectionId=$CONNECTION_ID&limit=25&offset=0&customerId=customer_id_123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Customer.io actions that support pagination

- [List Customer Messages](actions/list-customer-messages.md)
- [List Customers in a Segment](actions/list-customers-in-segment.md)
- [List Newsletters](actions/list-newsletters.md)
- [Search Customers](actions/search-customers.md)

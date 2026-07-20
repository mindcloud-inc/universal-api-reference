# Sharetribe Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Sharetribe expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sharetribe/latest/actions/query-availability-exceptions?connectionId=$CONNECTION_ID&limit=25&offset=0&listingId=string&start=2026-05-07T12%3A00%3A00.000Z&end=2026-05-07T12%3A00%3A00.000Z" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Sharetribe actions that support pagination

- [Query Availability Exceptions](actions/query-availability-exceptions.md)
- [Query Listings](actions/query-listings.md)
- [Query Stock Adjustments](actions/query-stock-adjustments.md)
- [Query Transactions](actions/query-transactions.md)
- [Query Users](actions/query-users.md)

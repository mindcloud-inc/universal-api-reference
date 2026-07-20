# Fidel API Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Fidel API expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fidelAPI/latest/actions/list-brands?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Fidel API actions that support pagination

- [List Brands](actions/list-brands.md)
- [List Cards](actions/list-cards.md)
- [List Locations](actions/list-locations.md)
- [List Locations by Brand](actions/list-locations-by-brand.md)
- [List MID Requests](actions/list-mid-requests.md)
- [List MIDs](actions/list-mids.md)
- [List Missing Transaction Requests](actions/list-missing-transaction-requests.md)
- [List Offers](actions/list-offers.md)
- [List Programs](actions/list-programs.md)
- [List Transactions by Card](actions/list-transactions-by-card.md)
- [List Transactions by Program](actions/list-transactions-by-program.md)

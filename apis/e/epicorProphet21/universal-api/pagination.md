# Epicor Prophet 21 Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Epicor Prophet 21 expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/epicorProphet21/latest/actions/list-addresses?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Epicor Prophet 21 actions that support pagination

- [List Addresses](actions/list-addresses.md)
- [List Contacts](actions/list-contacts.md)
- [List Customers](actions/list-customers.md)
- [List Quotes](actions/list-quotes.md)
- [List Sales Orders](actions/list-sales-orders.md)
- [Query Data View](actions/query-data-view.md)
- [Query Manifest Collection](actions/query-manifest-collection.md)
- [Query OData Table](actions/query-odata-table.md)
- [Query OData View](actions/query-odata-view.md)

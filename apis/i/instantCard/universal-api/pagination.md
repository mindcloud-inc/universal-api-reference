# InstantCard Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model InstantCard expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instantCard/latest/actions/list-addresses?connectionId=$CONNECTION_ID&limit=25&offset=0&organizationId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## InstantCard actions that support pagination

- [List Addresses](actions/list-addresses.md)
- [List Cards](actions/list-cards.md)
- [List Contacts](actions/list-contacts.md)
- [List Print Jobs](actions/list-print-jobs.md)
- [Search Cards](actions/search-cards.md)

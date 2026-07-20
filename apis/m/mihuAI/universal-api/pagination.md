# Mihu AI Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Mihu AI expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mihuAI/latest/actions/get-paginated-list-of-calls?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Mihu AI actions that support pagination

- [Get Paginated List of Calls](actions/get-paginated-list-of-calls.md)
- [Get Paginated List of Campaigns](actions/get-paginated-list-of-campaigns.md)
- [Get Paginated List of Contacts](actions/get-paginated-list-of-contacts.md)
- [Get Paginated List of Tasks](actions/get-paginated-list-of-tasks.md)

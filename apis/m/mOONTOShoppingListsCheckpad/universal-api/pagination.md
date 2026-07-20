# MOONTO Shopping Lists - Checkpad Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model MOONTO Shopping Lists - Checkpad expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mOONTOShoppingListsCheckpad/latest/actions/list-checkpad-events?connectionId=$CONNECTION_ID&limit=25&offset=0&checkpad_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## MOONTO Shopping Lists - Checkpad actions that support pagination

- [List Checkpad Events](actions/list-checkpad-events.md)
- [List Checkpads](actions/list-checkpads.md)
- [List List Events](actions/list-list-events.md)
- [List List Items](actions/list-list-items.md)
- [List Lists](actions/list-lists.md)

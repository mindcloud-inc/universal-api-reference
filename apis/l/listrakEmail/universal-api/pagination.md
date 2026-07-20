# Listrak Email Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Listrak Email expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/listrakEmail/latest/actions/get-message?connectionId=$CONNECTION_ID&limit=25&offset=0&listID=string&messageID=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Listrak Email actions that support pagination

- [Get Message](actions/get-message.md)
- [Get Transactional Message](actions/get-transactional-message.md)
- [List Messages](actions/list-messages.md)
- [List Transactional Messages](actions/list-transactional-messages.md)

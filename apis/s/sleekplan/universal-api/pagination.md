# Sleekplan Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Sleekplan expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sleekplan/latest/actions/list-comments?connectionId=$CONNECTION_ID&limit=25&offset=0&postId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Sleekplan actions that support pagination

- [List Comments](actions/list-comments.md)
- [List NPS Responses](actions/list-nps-responses.md)
- [List Posts](actions/list-posts.md)
- [List Satisfaction Responses](actions/list-satisfaction-responses.md)
- [List Update Satisfaction Responses](actions/list-update-satisfaction-responses.md)
- [List Updates](actions/list-updates.md)
- [List Users](actions/list-users.md)
- [List Votes](actions/list-votes.md)

# Missive Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Missive expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/missive/latest/actions/list-contact-books?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Missive actions that support pagination

- [List Contact Books](actions/list-contact-books.md)
- [List Organizations](actions/list-organizations.md)
- [List Responses](actions/list-responses.md)
- [List Teams](actions/list-teams.md)
- [List Users](actions/list-users.md)

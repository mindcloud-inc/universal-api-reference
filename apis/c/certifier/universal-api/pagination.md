# Certifier Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Certifier expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/certifier/latest/actions/list-credential-interactions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Certifier actions that support pagination

- [List Credential Interactions](actions/list-credential-interactions.md)
- [List Credentials](actions/list-credentials.md)
- [List Designs](actions/list-designs.md)
- [List Groups](actions/list-groups.md)

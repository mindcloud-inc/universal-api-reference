# CINCEL Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model CINCEL expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cINCEL/latest/actions/list-document-invites?connectionId=$CONNECTION_ID&limit=25&offset=0&team=string&folder=string&document=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## CINCEL actions that support pagination

- [List Document Invites](actions/list-document-invites.md)
- [List Folders](actions/list-folders.md)
- [List Team Users](actions/list-team-users.md)
- [List User Documents](actions/list-user-documents.md)
- [List User Teams](actions/list-user-teams.md)
- [List Users](actions/list-users.md)

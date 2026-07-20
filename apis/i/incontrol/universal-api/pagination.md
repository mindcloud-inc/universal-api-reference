# Incontrol Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Incontrol expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/incontrol/latest/actions/list-case-notes?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Incontrol actions that support pagination

- [List Case Notes](actions/list-case-notes.md)
- [List Cases](actions/list-cases.md)
- [List Documents](actions/list-documents.md)
- [List Drafts](actions/list-drafts.md)
- [List Form Templates](actions/list-form-templates.md)
- [List Forms](actions/list-forms.md)
- [List Local Data Connectors](actions/list-local-data-connectors.md)
- [List Notifications](actions/list-notifications.md)
- [List Organizations](actions/list-organizations.md)
- [List Tasks](actions/list-tasks.md)
- [List Users](actions/list-users.md)

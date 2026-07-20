# Damstra Forms Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Damstra Forms expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/damstraForms/latest/actions/list-actions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Damstra Forms actions that support pagination

- [List Actions](actions/list-actions.md)
- [List Drawing Annotations](actions/list-drawing-annotations.md)
- [List Drawing Views](actions/list-drawing-views.md)
- [List Drawings](actions/list-drawings.md)
- [List Forms](actions/list-forms.md)
- [List Memos](actions/list-memos.md)
- [List Projects](actions/list-projects.md)
- [List Punch Lists](actions/list-punch-lists.md)
- [List Templates](actions/list-templates.md)
- [List Users](actions/list-users.md)

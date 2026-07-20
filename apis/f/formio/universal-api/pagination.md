# Form.io Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Form.io expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/formio/latest/actions/list-admin-submissions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Form.io actions that support pagination

- [List Admin Submissions](actions/list-admin-submissions.md)
- [List Form Submissions](actions/list-form-submissions.md)
- [List Forms](actions/list-forms-all.md)
- [List Resource Forms](actions/list-resource-forms.md)
- [List Roles](actions/list-roles.md)
- [List Standard Forms](actions/list-standard-forms.md)
- [List User Submissions](actions/list-user-submissions.md)
- [Search Forms](actions/search-forms.md)
- [Search Roles](actions/search-roles.md)

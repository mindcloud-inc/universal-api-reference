# Paperform Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Paperform expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/paperform/latest/actions/list-form-partial-submissions?connectionId=$CONNECTION_ID&limit=25&offset=0&slugOrId=contact-us%20or%20123456" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Paperform actions that support pagination

- [List Form Partial Submissions](actions/list-form-partial-submissions.md)
- [List Form Submissions](actions/list-form-submissions.md)
- [List Forms](actions/list-forms.md)

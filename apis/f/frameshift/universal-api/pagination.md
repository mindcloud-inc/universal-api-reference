# Frameshift Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Frameshift expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/frameshift/latest/actions/list-all-sample-files?connectionId=$CONNECTION_ID&limit=25&offset=0&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Frameshift actions that support pagination

- [List All Sample Files](actions/list-all-sample-files.md)
- [List Project Activities](actions/list-project-activities.md)
- [List Project Files](actions/list-project-files.md)
- [List Project Variants](actions/list-project-variants.md)
- [List Projects](actions/list-projects.md)
- [List Sample Files](actions/list-sample-files.md)

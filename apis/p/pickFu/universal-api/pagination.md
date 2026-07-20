# PickFu Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model PickFu expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pickFu/latest/actions/get-survey-responses?connectionId=$CONNECTION_ID&limit=25&offset=0&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## PickFu actions that support pagination

- [Get Survey Responses](actions/get-survey-responses.md)
- [List Playbooks](actions/list-playbooks.md)
- [List Projects](actions/list-projects.md)
- [List Surveys](actions/list-surveys.md)
- [List Tags](actions/list-tags.md)

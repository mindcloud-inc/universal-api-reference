# SatisMeter Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model SatisMeter expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/satisMeter/latest/actions/list-project-responses?connectionId=$CONNECTION_ID&limit=25&offset=0&projectId=61fce0adea447e24ec27d606" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## SatisMeter actions that support pagination

- [List Project Responses](actions/list-project-responses.md)
- [List Survey Responses](actions/list-survey-responses.md)

# Simplesat Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Simplesat expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simplesat/latest/actions/list-customers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Simplesat actions that support pagination

- [List Customers](actions/list-customers.md)
- [List Questions](actions/list-questions.md)
- [List Surveys](actions/list-surveys.md)
- [Search Answers](actions/search-answers.md)
- [Search Responses](actions/search-responses.md)

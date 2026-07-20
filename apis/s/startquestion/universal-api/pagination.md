# Startquestion Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Startquestion expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/startquestion/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Startquestion actions that support pagination

- [List Contacts](actions/list-contacts.md)
- [List Survey Respondents](actions/list-survey-respondents.md)
- [List Surveys](actions/list-surveys.md)
- [Search Contacts](actions/search-contacts.md)
- [Search Survey Respondents](actions/search-survey-respondents.md)
- [Search Surveys](actions/search-surveys.md)

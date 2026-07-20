# CATS Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model CATS expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cATS/latest/actions/list-candidates?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## CATS actions that support pagination

- [List Candidates](actions/list-candidates.md)
- [List Companies](actions/list-companies.md)
- [List Contacts](actions/list-contacts.md)
- [List Job Statuses](actions/list-job-statuses.md)
- [List Jobs](actions/list-jobs.md)
- [List Pipelines](actions/list-pipelines.md)
- [List Users](actions/list-users.md)
- [Search Companies](actions/search-companies.md)
- [Search Contacts](actions/search-contacts.md)

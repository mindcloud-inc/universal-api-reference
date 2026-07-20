# Nicereply Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Nicereply expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nicereply/latest/actions/list-customers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Nicereply actions that support pagination

- [List Customers](actions/list-customers.md)
- [List Feedback Object Group Responses](actions/list-feedback-object-group-responses.md)
- [List Feedback Object Groups](actions/list-feedback-object-groups.md)
- [List Feedback Object Responses](actions/list-feedback-object-responses.md)
- [List Feedback Objects](actions/list-feedback-objects.md)
- [List Integrations](actions/list-integrations.md)
- [List Responses](actions/list-responses.md)
- [List Survey Responses](actions/list-survey-responses.md)
- [List Surveys](actions/list-surveys.md)
- [List Tags](actions/list-tags.md)
- [List Users](actions/list-users.md)

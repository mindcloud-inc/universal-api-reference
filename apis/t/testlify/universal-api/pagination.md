# Testlify Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Testlify expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/testlify/latest/actions/list-assessment-candidates?connectionId=$CONNECTION_ID&limit=25&offset=0&assessmentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Testlify actions that support pagination

- [List Assessment Candidates](actions/list-assessment-candidates.md)
- [List Assessments](actions/list-assessments.md)
- [List Candidates](actions/list-candidates.md)
- [List Questions](actions/list-questions.md)
- [List Test Libraries](actions/list-test-libraries.md)
- [List Workspace Users](actions/list-workspace-users.md)

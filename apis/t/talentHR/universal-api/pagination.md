# TalentHR Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model TalentHR expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/talentHR/latest/actions/get-directory?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## TalentHR actions that support pagination

- [Get Directory](actions/get-directory.md)
- [List Candidates](actions/list-candidates.md)
- [List Employee Assets](actions/list-employee-assets.md)
- [List Employee Completed Tasks](actions/list-employee-completed-tasks.md)
- [List Employee Pending Tasks](actions/list-employee-pending-tasks.md)
- [List Employee Time Off Requests](actions/list-employee-time-off-requests.md)
- [List Job Position Applicants](actions/list-job-position-applicants.md)

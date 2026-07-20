# Intruder Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Intruder expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/intruder/latest/actions/list-issue-occurrences?connectionId=$CONNECTION_ID&limit=25&offset=0&issueId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Intruder actions that support pagination

- [List Issue Occurrences](actions/list-issue-occurrences.md)
- [List Issues](actions/list-issues.md)
- [List Scan Schedules](actions/list-scan-schedules.md)
- [List Scans](actions/list-scans.md)
- [List Target API Schemas](actions/list-target-api-schemas.md)
- [List Target Authentications](actions/list-target-authentications.md)
- [List Targets](actions/list-targets.md)

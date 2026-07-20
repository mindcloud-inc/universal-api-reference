# Action1 Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Action1 expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/action1/latest/actions/get-report-rows?connectionId=$CONNECTION_ID&limit=25&offset=0&orgId=string&reportId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Action1 actions that support pagination

- [Get Report Rows](actions/get-report-rows.md)
- [List Audit Events](actions/list-audit-events.md)
- [List Automation Instances](actions/list-automation-instances.md)
- [List Automation Schedules](actions/list-automation-schedules.md)
- [List Endpoint Group Contents](actions/list-endpoint-group-contents.md)
- [List Endpoint Groups](actions/list-endpoint-groups.md)
- [List Endpoint Installed Software Rows](actions/list-endpoint-installed-software-rows.md)
- [List Endpoint Missing Updates](actions/list-endpoint-missing-updates.md)
- [List Endpoints](actions/list-endpoints.md)
- [List Installed Software Rows](actions/list-installed-software-rows.md)
- [List Missing Update Version Endpoints](actions/list-missing-update-version-endpoints.md)
- [List Missing Updates](actions/list-missing-updates.md)
- [List Vulnerabilities](actions/list-vulnerabilities.md)
- [List Vulnerability Endpoints](actions/list-vulnerability-endpoints.md)
- [List Vulnerability Remediations](actions/list-vulnerability-remediations.md)

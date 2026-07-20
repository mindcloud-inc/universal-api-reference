# YepCode Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model YepCode expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yepCode/latest/actions/get-execution-logs?connectionId=$CONNECTION_ID&limit=25&offset=0&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## YepCode actions that support pagination

- [Get execution logs](actions/get-execution-logs.md)
- [Get executions](actions/get-executions.md)
- [Get module version aliases](actions/get-module-version-aliases.md)
- [Get module versions](actions/get-module-versions.md)
- [Get modules](actions/get-modules.md)
- [Get process version aliases](actions/get-process-version-aliases.md)
- [Get process versions](actions/get-process-versions.md)
- [Get processes](actions/get-processes.md)
- [Get scheduled processes](actions/get-schedules.md)
- [Get variables](actions/get-variables.md)

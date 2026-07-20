# DevCycle Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model DevCycle expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/devCycle/latest/actions/list-audiences?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## DevCycle actions that support pagination

- [List Audiences](actions/list-audiences.md)
- [List Custom Properties](actions/list-custom-properties.md)
- [List Environments](actions/list-environments.md)
- [List Feature Audit Entries](actions/list-feature-audit-entries.md)
- [List Features](actions/list-features.md)
- [List Metrics](actions/list-metrics.md)
- [List Project Stale Features](actions/list-project-stale-features.md)
- [List Projects](actions/list-projects.md)
- [List Variables](actions/list-variables.md)
- [List Webhooks](actions/list-webhooks.md)

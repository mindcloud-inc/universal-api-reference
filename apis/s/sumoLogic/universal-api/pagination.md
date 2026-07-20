# Sumo Logic Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Sumo Logic expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sumoLogic/latest/actions/list-access-keys?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Sumo Logic actions that support pagination

- [List Access Keys](actions/list-access-keys.md)
- [List Connections](actions/list-connections.md)
- [List Data Deletion Rules](actions/list-data-deletion-rules.md)
- [List Data Masking Rules](actions/list-data-masking-rules.md)
- [List Dynamic Parsing Rules](actions/list-dynamic-parsing-rules.md)
- [List Field Extraction Rules](actions/list-field-extraction-rules.md)
- [List Health Events](actions/list-health-events.md)
- [List Ingest Budgets](actions/list-ingest-budgets.md)
- [List Log Data Forwarding Rules](actions/list-log-data-forwarding-rules.md)
- [List Log Searches](actions/list-log-searches.md)
- [List Partitions](actions/list-partitions.md)
- [List Roles](actions/list-roles.md)
- [List Roles V2](actions/list-roles-v2.md)
- [List Scheduled Views](actions/list-scheduled-views.md)
- [List Transformation Rules](actions/list-transformation-rules.md)
- [List Users](actions/list-users.md)

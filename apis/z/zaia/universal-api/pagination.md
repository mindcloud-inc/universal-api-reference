# Zaia Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Zaia expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zaia/latest/actions/list-agents?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Zaia actions that support pagination

- [List Agents](actions/list-agents.md)
- [List Channels](actions/list-channels.md)
- [List Components](actions/list-components.md)
- [List Connections](actions/list-connections.md)
- [List Datagrids](actions/list-datagrids.md)
- [List Datasets](actions/list-datasets.md)
- [List Executions](actions/list-executions.md)
- [List External Users](actions/list-external-users.md)
- [List LLM Providers](actions/list-llm-providers.md)
- [List MCPs](actions/list-mcps.md)
- [List Responders](actions/list-responders.md)
- [List Squads](actions/list-squads.md)
- [List Tags](actions/list-tags.md)
- [List Ticketing Teams](actions/list-ticketing-teams.md)

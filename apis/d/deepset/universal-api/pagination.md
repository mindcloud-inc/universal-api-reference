# Deepset Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Deepset expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deepset/latest/actions/get-pipeline-logs?connectionId=$CONNECTION_ID&limit=25&offset=0&pipelineName=Ava%20Chen&workspaceName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Deepset actions that support pagination

- [Get Pipeline Logs](actions/get-pipeline-logs.md)
- [Get Roles](actions/get-roles.md)
- [Get Search Sessions](actions/get-search-sessions.md)
- [Get Users](actions/get-users.md)
- [List Datasets](actions/list-datasets.md)
- [List Files](actions/list-files.md)
- [List Indexes](actions/list-indexes.md)
- [List Pipelines](actions/list-pipelines.md)
- [List Workspaces](actions/list-workspaces.md)

# Ringg AI Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Ringg AI expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ringgAI/latest/actions/download-call-history?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Ringg AI actions that support pagination

- [Download Call History](actions/download-call-history.md)
- [Get All Campaigns](actions/get-all-campaigns.md)
- [Get Assistants](actions/get-assistants.md)
- [Get Call History](actions/get-call-history.md)
- [Get Workspace Numbers](actions/get-workspace-numbers.md)
- [List Workspace Users](actions/list-workspace-users.md)

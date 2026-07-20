# Content Snare Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Content Snare expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/contentSnare/latest/actions/list-client-companies?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Content Snare actions that support pagination

- [List Client Companies](actions/list-client-companies.md)
- [List Clients](actions/list-clients.md)
- [List Communications Schedules](actions/list-communications-schedules.md)
- [List Folders](actions/list-folders.md)
- [List Page Templates](actions/list-page-templates.md)
- [List Request Templates](actions/list-request-templates.md)
- [List Requests](actions/list-requests.md)
- [List Section Templates](actions/list-section-templates.md)
- [List Team Members](actions/list-team-members.md)
- [List Webhooks](actions/list-webhooks.md)

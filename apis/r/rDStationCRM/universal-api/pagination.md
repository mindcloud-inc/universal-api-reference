# RD Station CRM Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model RD Station CRM expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rDStationCRM/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## RD Station CRM actions that support pagination

- [List Contacts](actions/list-contacts.md)
- [List Deals](actions/list-deals.md)
- [List Organizations](actions/list-organizations.md)
- [List Pipeline Stages](actions/list-pipeline-stages.md)
- [List Pipelines](actions/list-pipelines.md)
- [List Sources](actions/list-sources.md)
- [List Tasks](actions/list-tasks.md)
- [List Users](actions/list-users.md)

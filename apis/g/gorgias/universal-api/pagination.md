# Gorgias Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Gorgias expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gorgias/latest/actions/list-custom-fields?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Gorgias actions that support pagination

- [List Custom Fields](actions/list-custom-fields.md)
- [List Customers](actions/list-customers.md)
- [List Events](actions/list-events.md)
- [List Integrations](actions/list-integrations.md)
- [List Jobs](actions/list-jobs.md)
- [List Macros](actions/list-macros.md)
- [List Messages](actions/list-messages.md)
- [List Rules](actions/list-rules.md)
- [List Surveys](actions/list-surveys.md)
- [List Tags](actions/list-tags.md)
- [List Teams](actions/list-teams.md)
- [List Tickets](actions/list-tickets.md)
- [List Users](actions/list-users.md)
- [List Views](actions/list-views.md)
- [List Widgets](actions/list-widgets.md)
- [Search Resources](actions/search-resources.md)

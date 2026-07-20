# Qualiobee Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Qualiobee expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/qualiobee/latest/actions/list-conventions?connectionId=$CONNECTION_ID&limit=25&offset=0&organizationUuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Qualiobee actions that support pagination

- [List Conventions](actions/list-conventions.md)
- [List Customers](actions/list-customers.md)
- [List Formations](actions/list-formations.md)
- [List Learners](actions/list-learners.md)
- [List Locations](actions/list-locations.md)
- [List Sessions](actions/list-sessions.md)

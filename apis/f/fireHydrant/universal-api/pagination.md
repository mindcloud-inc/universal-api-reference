# FireHydrant Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model FireHydrant expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fireHydrant/latest/actions/list-environments?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## FireHydrant actions that support pagination

- [List Environments](actions/list-environments.md)
- [List Functionalities](actions/list-functionalities.md)
- [List Incident Events](actions/list-incident-events.md)
- [List Incident Roles](actions/list-incident-roles.md)
- [List Incident Tasks](actions/list-incident-tasks.md)
- [List Incident Types](actions/list-incident-types.md)
- [List Incidents](actions/list-incidents.md)
- [List Priorities](actions/list-priorities.md)
- [List Runbooks](actions/list-runbooks.md)
- [List Services](actions/list-services.md)
- [List Severities](actions/list-severities.md)
- [List Teams](actions/list-teams.md)
- [List Users](actions/list-users.md)

# Prisma Postgres Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Prisma Postgres expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/prismaPostgres/latest/actions/list-connections?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Prisma Postgres actions that support pagination

- [List Connections](actions/list-connections.md)
- [List Database Connections](actions/list-database-connections.md)
- [List Databases](actions/list-databases.md)
- [List Integrations](actions/list-integrations.md)
- [List Project Databases](actions/list-project-databases.md)
- [List Projects](actions/list-projects.md)
- [List Workspace Integrations](actions/list-workspace-integrations.md)
- [List Workspaces](actions/list-workspaces.md)

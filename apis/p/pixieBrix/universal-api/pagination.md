# PixieBrix Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model PixieBrix expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pixieBrix/latest/actions/list-database-assets?connectionId=$CONNECTION_ID&limit=25&offset=0&databasePk=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## PixieBrix actions that support pagination

- [List Database Assets](actions/list-database-assets.md)
- [List Database Records](actions/list-database-records.md)
- [List Databases](actions/list-databases.md)
- [List Deployments](actions/list-deployments.md)
- [List Groups](actions/list-groups.md)
- [List Organization Memberships](actions/list-organization-memberships.md)
- [List Organizations](actions/list-organizations.md)
- [List Package Versions](actions/list-package-versions.md)
- [List Packages](actions/list-packages.md)
- [List Registry Bricks](actions/list-registry-bricks.md)

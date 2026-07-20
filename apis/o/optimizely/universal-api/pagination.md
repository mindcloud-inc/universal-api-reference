# Optimizely Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Optimizely expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/optimizely/latest/actions/list-attributes?connectionId=$CONNECTION_ID&limit=25&offset=0&projectId=4844790198566912" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Optimizely actions that support pagination

- [List Attributes](actions/list-attributes.md)
- [List Audiences](actions/list-audiences.md)
- [List Campaigns](actions/list-campaigns.md)
- [List Changes](actions/list-changes.md)
- [List Environments](actions/list-environments.md)
- [List Events](actions/list-events.md)
- [List Experiments](actions/list-experiments.md)
- [List Extensions](actions/list-extensions.md)
- [List Features](actions/list-features.md)
- [List Groups](actions/list-groups.md)
- [List Pages](actions/list-pages.md)
- [List Projects](actions/list-projects.md)
- [List Sections](actions/list-sections.md)
- [List Subject Access Requests](actions/list-subject-access-requests.md)
- [List Webhooks](actions/list-webhooks.md)
- [Search Entities](actions/search-entities.md)

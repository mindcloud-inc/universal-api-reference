# Braintrust Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Braintrust expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/braintrust/latest/actions/list-datasets?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Braintrust actions that support pagination

- [List Datasets](actions/list-datasets.md)
- [List Experiments](actions/list-experiments.md)
- [List Functions](actions/list-functions.md)
- [List Organizations](actions/list-organizations.md)
- [List Project Scores](actions/list-project-scores.md)
- [List Project Tags](actions/list-project-tags.md)
- [List Projects](actions/list-projects.md)
- [List Prompts](actions/list-prompts.md)
- [List Users](actions/list-users.md)
- [List Views](actions/list-views.md)

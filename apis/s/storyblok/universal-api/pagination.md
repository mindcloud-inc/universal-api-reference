# Storyblok Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Storyblok expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/storyblok/latest/actions/filter-stories?connectionId=$CONNECTION_ID&limit=25&offset=0&filterQuery=component%5Bin%5D%3Dpage" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Storyblok actions that support pagination

- [Filter Stories](actions/filter-stories.md)
- [List Datasource Entries](actions/list-datasource-entries.md)
- [List Datasources](actions/list-datasources.md)
- [List Links](actions/list-links.md)
- [List Links in Folder](actions/list-links-in-folder.md)
- [List Stories](actions/list-stories.md)
- [List Stories by Content Type](actions/list-stories-by-content-type.md)
- [List Stories by Language](actions/list-stories-by-language.md)
- [List Stories by Tag](actions/list-stories-by-tag.md)
- [List Stories by UUIDs](actions/list-stories-by-uui-ds.md)
- [List Stories in Folder](actions/list-stories-in-folder.md)
- [List Stories in Workflow Stage](actions/list-stories-in-workflow-stage.md)
- [List Stories with Resolved Relations](actions/list-stories-with-resolved-relations.md)
- [Search Stories](actions/search-stories.md)
- [Sort Stories](actions/sort-stories.md)

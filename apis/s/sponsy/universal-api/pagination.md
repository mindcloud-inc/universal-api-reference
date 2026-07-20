# Sponsy Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Sponsy expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sponsy/latest/actions/list-publication-placements?connectionId=$CONNECTION_ID&limit=25&offset=0&publicationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Sponsy actions that support pagination

- [List Publication Placements](actions/list-publication-placements.md)
- [List Publication Slots](actions/list-publication-slots.md)
- [List Publication Statuses](actions/list-publication-statuses.md)
- [List Publications](actions/list-publications.md)

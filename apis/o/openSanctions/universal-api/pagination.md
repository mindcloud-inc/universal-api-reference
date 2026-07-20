# OpenSanctions Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model OpenSanctions expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openSanctions/latest/actions/list-adjacent-entities?connectionId=$CONNECTION_ID&limit=25&offset=0&entity_id=Q7747" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## OpenSanctions actions that support pagination

- [List Adjacent Entities](actions/list-adjacent-entities.md)
- [List Adjacent Entities By Property](actions/list-adjacent-entities-by-property.md)
- [List Entity Statements](actions/list-entity-statements.md)
- [Search Entities](actions/search-entities.md)
